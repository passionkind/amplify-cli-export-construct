
## amplify-cli-export-backend

[![build](https://github.com/aws-amplify/amplify-cli-export-construct/actions/workflows/build.yml/badge.svg)](https://github.com/aws-amplify/amplify-cli-export-construct/actions/workflows/build.yml)

[![Integration Tests](https://github.com/aws-amplify/amplify-cli-export-construct/actions/workflows/integration-test.yml/badge.svg?branch=main)](https://github.com/aws-amplify/amplify-cli-export-construct/actions/workflows/integration-test.yml)


This CDK construct is used to include the CloudFormation resources generated by [Amplify CLI Export command](https://docs.amplify.aws/cli/). The construct handles assets and CloudFormation files. It offers abstractions over the Amplify CLI generated cloud resources.

The library is published under the following

|Language	|Repository	|
|---	|---	|
|Typescript/Javascript	|	|
|Python	|	|
|.Net	|	|
|Java	|	|

### Usage

Install via NPM:


```bash
npm i @aws-amplify/cli-export-backend@latest
```


Add to your CDK app:


```js
import { AmplifyExportBackend }  from 'cli-export-backend';
...
const amplifyExport = new AmplifyExportBackend(app, 'AmplifyExportedBackend', {
  path: './amplify-export-myAmplifyApp',
  stage: 'dev', 
});


```



#### Construct Props

The construct props extend [stack props](https://docs.aws.amazon.com/cdk/api/latest/docs/@aws-cdk_core.StackProps.html) and can be used to override the root stack properties.

|Name	|Type	|Description	|Required	|Default	|
|---	|---	|---	|---	|---	|
|path	|String	|You can use the absolute or the relative path to the location of the folder. When using relative paths it's important to note that the path is relative to the root of your CDK application	|Yes	|undefined	|
|stage	|String	|This works similar to Amplify CLI's environment names. The construct makes modification to be able to integrate into the CDK app.	|No	|dev	|


Deploy this to your account

```bash
cdk deploy 
```



### Contributing

We welcome community contributions and pull requests.

### Security

See [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) for more information.

### License

This project is licensed under the Apache-2.0 License.

