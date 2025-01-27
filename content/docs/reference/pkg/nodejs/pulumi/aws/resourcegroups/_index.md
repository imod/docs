---
title: "Module resourcegroups"
title_tag: "Module resourcegroups | Package @pulumi/aws | Node.js SDK"
linktitle: "resourcegroups"
meta_desc: "Explore members of the resourcegroups module in the @pulumi/aws package."
git_sha: "6c9e985f93682e9b4056b497c1a31a75fd7884fc"
block_external_search_index: true
---

<!-- WARNING: this page was generated by a tool. Do not edit it by hand. -->
<!-- To change it, please see https://github.com/pulumi/docs/tree/master/tools/tscdocgen. -->

{{< resource-docs-alert "aws" >}}




<h3>Resources</h3>
<ul class="api">
    <li><a href="#Group"><span class="symbol resource"></span>Group</a></li>
</ul>


<h3>Others</h3>
<ul class="api">
    <li><a href="#GroupArgs"><span class="symbol api"></span>GroupArgs</a></li>
    <li><a href="#GroupState"><span class="symbol api"></span>GroupState</a></li>
</ul>


<h2 id="resources">Resources</h2>
<h3 class="pdoc-module-header" id="Group" data-link-title="Group">
    <a href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/resourcegroups/group.ts#L43">
        Resource <strong>Group</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>class</span> <span class='nx'>Group</span> <span class='kr'>extends</span> <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResource'>CustomResource</a></code></pre>

Provides a Resource Group.

#### Example Usage

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws from "@pulumi/aws";

const test = new aws.resourcegroups.Group("test", {
    resourceQuery: {
        query: `{
  "ResourceTypeFilters": [
    "AWS::EC2::Instance"
  ],
  "TagFilters": [
    {
      "Key": "Stage",
      "Values": ["Test"]
    }
  ]
}
`,
    },
});
```

#### Import

Resource groups can be imported using the `name`, e.g.

```sh
 $ pulumi import aws:resourcegroups/group:Group foo resource-group-name
```

<h4 class="pdoc-member-header" id="Group-constructor">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/resourcegroups/group.ts#L90"> <b>constructor</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span><span class='kd'>new</span> Group(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, args: <a href='#GroupArgs'>GroupArgs</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>)</code></pre>


Create a Group resource with the given unique name, arguments, and options.

* `name` The _unique_ name of the resource.
* `args` The arguments to use to populate this resource&#39;s properties.
* `opts` A bag of options that control this resource&#39;s behavior.

<h4 class="pdoc-member-header" id="Group-get">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/resourcegroups/group.ts#L53">method <b>get</b></a>
</h4>


<pre class="highlight"><code><span class='kd'>public static </span>get(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>pulumi.ID</a>&gt;, state?: <a href='#GroupState'>GroupState</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>): <a href='#Group'>Group</a></code></pre>


Get an existing Group resource's state with the given name, ID, and optional extra
properties used to qualify the lookup.

<h4 class="pdoc-member-header" id="Group-getProvider">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/resourcegroups/group.ts#L43">method <b>getProvider</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>getProvider(moduleMember: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>): <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ProviderResource'>ProviderResource</a> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span></code></pre>

<h4 class="pdoc-member-header" id="Group-isInstance">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/resourcegroups/group.ts#L64">method <b>isInstance</b></a>
</h4>


<pre class="highlight"><code><span class='kd'>public static </span>isInstance(obj: <span class='kd'><a href='https://www.typescriptlang.org/docs/handbook/basic-types.html#any'>any</a></span>): obj is Group</code></pre>


Returns true if the given object is an instance of Group.  This is designed to work even
when multiple copies of the Pulumi SDK have been loaded into the same process.

<h4 class="pdoc-member-header" id="Group-arn">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/resourcegroups/group.ts#L74">property <b>arn</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>arn: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The ARN assigned by AWS for this resource group.

<h4 class="pdoc-member-header" id="Group-description">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/resourcegroups/group.ts#L78">property <b>description</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>description: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span>&gt;;</code></pre>

A description of the resource group.

<h4 class="pdoc-member-header" id="Group-id">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/resourcegroups/group.ts#L43">property <b>id</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>ID</a>&gt;;</code></pre>

id is the provider-assigned unique ID for this managed resource.  It is set during
deployments and may be missing (undefined) during planning phases.

<h4 class="pdoc-member-header" id="Group-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/resourcegroups/group.ts#L82">property <b>name</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>name: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The resource group's name. A resource group name can have a maximum of 127 characters, including letters, numbers, hyphens, dots, and underscores. The name cannot start with `AWS` or `aws`.

<h4 class="pdoc-member-header" id="Group-resourceQuery">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/resourcegroups/group.ts#L86">property <b>resourceQuery</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>resourceQuery: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/aws/types/output/#GroupResourceQuery'>GroupResourceQuery</a>&gt;;</code></pre>

A `resourceQuery` block. Resource queries are documented below.

<h4 class="pdoc-member-header" id="Group-tags">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/resourcegroups/group.ts#L90">property <b>tags</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>tags: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;{[key: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>]: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>} | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span>&gt;;</code></pre>

Key-value map of resource tags

<h4 class="pdoc-member-header" id="Group-urn">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/resourcegroups/group.ts#L43">property <b>urn</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>urn: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#URN'>URN</a>&gt;;</code></pre>

urn is the stable logical URN used to distinctly address a resource, both before and after
deployments.



<h2 id="apis">Others</h2>
<h3 class="pdoc-module-header" id="GroupArgs" data-link-title="GroupArgs">
    <a href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/resourcegroups/group.ts#L160">
        interface <strong>GroupArgs</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>GroupArgs</span></code></pre>

The set of arguments for constructing a Group resource.

<h4 class="pdoc-member-header" id="GroupArgs-description">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/resourcegroups/group.ts#L164">property <b>description</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>description?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

A description of the resource group.

<h4 class="pdoc-member-header" id="GroupArgs-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/resourcegroups/group.ts#L168">property <b>name</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>name?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The resource group's name. A resource group name can have a maximum of 127 characters, including letters, numbers, hyphens, dots, and underscores. The name cannot start with `AWS` or `aws`.

<h4 class="pdoc-member-header" id="GroupArgs-resourceQuery">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/resourcegroups/group.ts#L172">property <b>resourceQuery</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>resourceQuery: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/aws/types/input/#GroupResourceQuery'>GroupResourceQuery</a>&gt;;</code></pre>

A `resourceQuery` block. Resource queries are documented below.

<h4 class="pdoc-member-header" id="GroupArgs-tags">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/resourcegroups/group.ts#L176">property <b>tags</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>tags?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;{[key: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>]: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;}&gt;;</code></pre>

Key-value map of resource tags

<h3 class="pdoc-module-header" id="GroupState" data-link-title="GroupState">
    <a href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/resourcegroups/group.ts#L134">
        interface <strong>GroupState</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>GroupState</span></code></pre>

Input properties used for looking up and filtering Group resources.

<h4 class="pdoc-member-header" id="GroupState-arn">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/resourcegroups/group.ts#L138">property <b>arn</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>arn?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The ARN assigned by AWS for this resource group.

<h4 class="pdoc-member-header" id="GroupState-description">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/resourcegroups/group.ts#L142">property <b>description</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>description?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

A description of the resource group.

<h4 class="pdoc-member-header" id="GroupState-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/resourcegroups/group.ts#L146">property <b>name</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>name?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The resource group's name. A resource group name can have a maximum of 127 characters, including letters, numbers, hyphens, dots, and underscores. The name cannot start with `AWS` or `aws`.

<h4 class="pdoc-member-header" id="GroupState-resourceQuery">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/resourcegroups/group.ts#L150">property <b>resourceQuery</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>resourceQuery?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/aws/types/input/#GroupResourceQuery'>GroupResourceQuery</a>&gt;;</code></pre>

A `resourceQuery` block. Resource queries are documented below.

<h4 class="pdoc-member-header" id="GroupState-tags">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/resourcegroups/group.ts#L154">property <b>tags</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>tags?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;{[key: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>]: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;}&gt;;</code></pre>

Key-value map of resource tags

