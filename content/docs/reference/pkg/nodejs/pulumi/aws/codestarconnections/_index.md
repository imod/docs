---
title: "Module codestarconnections"
title_tag: "Module codestarconnections | Package @pulumi/aws | Node.js SDK"
linktitle: "codestarconnections"
meta_desc: "Explore members of the codestarconnections module in the @pulumi/aws package."
git_sha: "6c9e985f93682e9b4056b497c1a31a75fd7884fc"
block_external_search_index: true
---

<!-- WARNING: this page was generated by a tool. Do not edit it by hand. -->
<!-- To change it, please see https://github.com/pulumi/docs/tree/master/tools/tscdocgen. -->

{{< resource-docs-alert "aws" >}}




<h3>Resources</h3>
<ul class="api">
    <li><a href="#Connection"><span class="symbol resource"></span>Connection</a></li>
</ul>


<h3>Others</h3>
<ul class="api">
    <li><a href="#ConnectionArgs"><span class="symbol api"></span>ConnectionArgs</a></li>
    <li><a href="#ConnectionState"><span class="symbol api"></span>ConnectionState</a></li>
</ul>


<h2 id="resources">Resources</h2>
<h3 class="pdoc-module-header" id="Connection" data-link-title="Connection">
    <a href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/codestarconnections/connection.ts#L63">
        Resource <strong>Connection</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>class</span> <span class='nx'>Connection</span> <span class='kr'>extends</span> <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResource'>CustomResource</a></code></pre>

Provides a CodeStar Connection.

> **NOTE:** The `aws.codestarconnections.Connection` resource is created in the state `PENDING`. Authentication with the connection provider must be completed in the AWS Console.

#### Example Usage

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws from "@pulumi/aws";

const exampleConnection = new aws.codestarconnections.Connection("exampleConnection", {
    connectionName: "example-connection",
    providerType: "Bitbucket",
});
const examplePipeline = new aws.codepipeline.Pipeline("examplePipeline", {
    roleArn: aws_iam_role.codepipeline_role.arn,
    artifactStore: {},
    stages: [
        {
            name: "Source",
            actions: [{
                name: "Source",
                category: "Source",
                owner: "AWS",
                provider: "CodeStarSourceConnection",
                version: "1",
                outputArtifacts: ["source_output"],
                configuration: {
                    Owner: "my-organization",
                    ConnectionArn: exampleConnection.arn,
                    Repo: "foo/test",
                    Branch: "master",
                },
            }],
        },
        {
            name: "Build",
            actions: [{}],
        },
        {
            name: "Deploy",
            actions: [{}],
        },
    ],
});
```

#### Import

CodeStar connections can be imported using the ARN, e.g.

```sh
 $ pulumi import aws:codestarconnections/connection:Connection test-connection arn:aws:codestar-connections:us-west-1:0123456789:connection/79d4d357-a2ee-41e4-b350-2fe39ae59448
```

<h4 class="pdoc-member-header" id="Connection-constructor">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/codestarconnections/connection.ts#L106"> <b>constructor</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span><span class='kd'>new</span> Connection(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, args: <a href='#ConnectionArgs'>ConnectionArgs</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>)</code></pre>


Create a Connection resource with the given unique name, arguments, and options.

* `name` The _unique_ name of the resource.
* `args` The arguments to use to populate this resource&#39;s properties.
* `opts` A bag of options that control this resource&#39;s behavior.

<h4 class="pdoc-member-header" id="Connection-get">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/codestarconnections/connection.ts#L73">method <b>get</b></a>
</h4>


<pre class="highlight"><code><span class='kd'>public static </span>get(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>pulumi.ID</a>&gt;, state?: <a href='#ConnectionState'>ConnectionState</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>): <a href='#Connection'>Connection</a></code></pre>


Get an existing Connection resource's state with the given name, ID, and optional extra
properties used to qualify the lookup.

<h4 class="pdoc-member-header" id="Connection-getProvider">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/codestarconnections/connection.ts#L63">method <b>getProvider</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>getProvider(moduleMember: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>): <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ProviderResource'>ProviderResource</a> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span></code></pre>

<h4 class="pdoc-member-header" id="Connection-isInstance">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/codestarconnections/connection.ts#L84">method <b>isInstance</b></a>
</h4>


<pre class="highlight"><code><span class='kd'>public static </span>isInstance(obj: <span class='kd'><a href='https://www.typescriptlang.org/docs/handbook/basic-types.html#any'>any</a></span>): obj is Connection</code></pre>


Returns true if the given object is an instance of Connection.  This is designed to work even
when multiple copies of the Pulumi SDK have been loaded into the same process.

<h4 class="pdoc-member-header" id="Connection-arn">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/codestarconnections/connection.ts#L94">property <b>arn</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>arn: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The codestar connection ARN.

<h4 class="pdoc-member-header" id="Connection-connectionStatus">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/codestarconnections/connection.ts#L98">property <b>connectionStatus</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>connectionStatus: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The codestar connection status. Possible values are `PENDING`, `AVAILABLE` and `ERROR`.

<h4 class="pdoc-member-header" id="Connection-id">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/codestarconnections/connection.ts#L63">property <b>id</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>ID</a>&gt;;</code></pre>

id is the provider-assigned unique ID for this managed resource.  It is set during
deployments and may be missing (undefined) during planning phases.

<h4 class="pdoc-member-header" id="Connection-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/codestarconnections/connection.ts#L102">property <b>name</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>name: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The name of the connection to be created. The name must be unique in the calling AWS account. Changing `name` will create a new resource.

<h4 class="pdoc-member-header" id="Connection-providerType">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/codestarconnections/connection.ts#L106">property <b>providerType</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>providerType: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The name of the external provider where your third-party code repository is configured. Valid values are `Bitbucket`, `GitHub`, or `GitHubEnterpriseServer`. Changing `providerType` will create a new resource.

<h4 class="pdoc-member-header" id="Connection-urn">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/codestarconnections/connection.ts#L63">property <b>urn</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>urn: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#URN'>URN</a>&gt;;</code></pre>

urn is the stable logical URN used to distinctly address a resource, both before and after
deployments.



<h2 id="apis">Others</h2>
<h3 class="pdoc-module-header" id="ConnectionArgs" data-link-title="ConnectionArgs">
    <a href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/codestarconnections/connection.ts#L170">
        interface <strong>ConnectionArgs</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>ConnectionArgs</span></code></pre>

The set of arguments for constructing a Connection resource.

<h4 class="pdoc-member-header" id="ConnectionArgs-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/codestarconnections/connection.ts#L174">property <b>name</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>name?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The name of the connection to be created. The name must be unique in the calling AWS account. Changing `name` will create a new resource.

<h4 class="pdoc-member-header" id="ConnectionArgs-providerType">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/codestarconnections/connection.ts#L178">property <b>providerType</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>providerType: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The name of the external provider where your third-party code repository is configured. Valid values are `Bitbucket`, `GitHub`, or `GitHubEnterpriseServer`. Changing `providerType` will create a new resource.

<h3 class="pdoc-module-header" id="ConnectionState" data-link-title="ConnectionState">
    <a href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/codestarconnections/connection.ts#L148">
        interface <strong>ConnectionState</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>ConnectionState</span></code></pre>

Input properties used for looking up and filtering Connection resources.

<h4 class="pdoc-member-header" id="ConnectionState-arn">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/codestarconnections/connection.ts#L152">property <b>arn</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>arn?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The codestar connection ARN.

<h4 class="pdoc-member-header" id="ConnectionState-connectionStatus">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/codestarconnections/connection.ts#L156">property <b>connectionStatus</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>connectionStatus?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The codestar connection status. Possible values are `PENDING`, `AVAILABLE` and `ERROR`.

<h4 class="pdoc-member-header" id="ConnectionState-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/codestarconnections/connection.ts#L160">property <b>name</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>name?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The name of the connection to be created. The name must be unique in the calling AWS account. Changing `name` will create a new resource.

<h4 class="pdoc-member-header" id="ConnectionState-providerType">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/codestarconnections/connection.ts#L164">property <b>providerType</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>providerType?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The name of the external provider where your third-party code repository is configured. Valid values are `Bitbucket`, `GitHub`, or `GitHubEnterpriseServer`. Changing `providerType` will create a new resource.

