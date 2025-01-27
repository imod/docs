---
title: "Module proximity"
title_tag: "Module proximity | Package @pulumi/azure | Node.js SDK"
linktitle: "proximity"
meta_desc: "Explore members of the proximity module in the @pulumi/azure package."
git_sha: "759289fd9b3a0ab07d1ece84247638497d4bb8ba"
block_external_search_index: true
---

<!-- WARNING: this page was generated by a tool. Do not edit it by hand. -->
<!-- To change it, please see https://github.com/pulumi/docs/tree/master/tools/tscdocgen. -->

{{< resource-docs-alert "azure" >}}




<h3>Resources</h3>
<ul class="api">
    <li><a href="#PlacementGroup"><span class="symbol resource"></span>PlacementGroup</a></li>
</ul>

<h3>Functions</h3>
<ul class="api">
    <li><a href="#getPlacementGroup"><span class="symbol function"></span>getPlacementGroup</a></li>
</ul>

<h3>Others</h3>
<ul class="api">
    <li><a href="#GetPlacementGroupArgs"><span class="symbol api"></span>GetPlacementGroupArgs</a></li>
    <li><a href="#GetPlacementGroupResult"><span class="symbol api"></span>GetPlacementGroupResult</a></li>
    <li><a href="#PlacementGroupArgs"><span class="symbol api"></span>PlacementGroupArgs</a></li>
    <li><a href="#PlacementGroupState"><span class="symbol api"></span>PlacementGroupState</a></li>
</ul>


<h2 id="resources">Resources</h2>
<h3 class="pdoc-module-header" id="PlacementGroup" data-link-title="PlacementGroup">
    <a href="https://github.com/pulumi/pulumi-azure/blob/759289fd9b3a0ab07d1ece84247638497d4bb8ba/sdk/nodejs/proximity/placementGroup.ts#L34">
        Resource <strong>PlacementGroup</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>class</span> <span class='nx'>PlacementGroup</span> <span class='kr'>extends</span> <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResource'>CustomResource</a></code></pre>

Manages a proximity placement group for virtual machines, virtual machine scale sets and availability sets.

#### Example Usage

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as azure from "@pulumi/azure";

const exampleResourceGroup = new azure.core.ResourceGroup("exampleResourceGroup", {location: "West US"});
const examplePlacementGroup = new azure.proximity.PlacementGroup("examplePlacementGroup", {
    location: exampleResourceGroup.location,
    resourceGroupName: exampleResourceGroup.name,
    tags: {
        environment: "Production",
    },
});
```

#### Import

Proximity Placement Groups can be imported using the `resource id`, e.g.

```sh
 $ pulumi import azure:proximity/placementGroup:PlacementGroup example /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/example-rg/providers/Microsoft.Compute/proximityPlacementGroups/example-ppg
```

<h4 class="pdoc-member-header" id="PlacementGroup-constructor">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/759289fd9b3a0ab07d1ece84247638497d4bb8ba/sdk/nodejs/proximity/placementGroup.ts#L77"> <b>constructor</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span><span class='kd'>new</span> PlacementGroup(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, args: <a href='#PlacementGroupArgs'>PlacementGroupArgs</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>)</code></pre>


Create a PlacementGroup resource with the given unique name, arguments, and options.

* `name` The _unique_ name of the resource.
* `args` The arguments to use to populate this resource&#39;s properties.
* `opts` A bag of options that control this resource&#39;s behavior.

<h4 class="pdoc-member-header" id="PlacementGroup-get">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/759289fd9b3a0ab07d1ece84247638497d4bb8ba/sdk/nodejs/proximity/placementGroup.ts#L44">method <b>get</b></a>
</h4>


<pre class="highlight"><code><span class='kd'>public static </span>get(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>pulumi.ID</a>&gt;, state?: <a href='#PlacementGroupState'>PlacementGroupState</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>): <a href='#PlacementGroup'>PlacementGroup</a></code></pre>


Get an existing PlacementGroup resource's state with the given name, ID, and optional extra
properties used to qualify the lookup.

<h4 class="pdoc-member-header" id="PlacementGroup-getProvider">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/759289fd9b3a0ab07d1ece84247638497d4bb8ba/sdk/nodejs/proximity/placementGroup.ts#L34">method <b>getProvider</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>getProvider(moduleMember: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>): <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ProviderResource'>ProviderResource</a> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span></code></pre>

<h4 class="pdoc-member-header" id="PlacementGroup-isInstance">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/759289fd9b3a0ab07d1ece84247638497d4bb8ba/sdk/nodejs/proximity/placementGroup.ts#L55">method <b>isInstance</b></a>
</h4>


<pre class="highlight"><code><span class='kd'>public static </span>isInstance(obj: <span class='kd'><a href='https://www.typescriptlang.org/docs/handbook/basic-types.html#any'>any</a></span>): obj is PlacementGroup</code></pre>


Returns true if the given object is an instance of PlacementGroup.  This is designed to work even
when multiple copies of the Pulumi SDK have been loaded into the same process.

<h4 class="pdoc-member-header" id="PlacementGroup-id">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/759289fd9b3a0ab07d1ece84247638497d4bb8ba/sdk/nodejs/proximity/placementGroup.ts#L34">property <b>id</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>ID</a>&gt;;</code></pre>

id is the provider-assigned unique ID for this managed resource.  It is set during
deployments and may be missing (undefined) during planning phases.

<h4 class="pdoc-member-header" id="PlacementGroup-location">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/759289fd9b3a0ab07d1ece84247638497d4bb8ba/sdk/nodejs/proximity/placementGroup.ts#L65">property <b>location</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>location: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Specifies the supported Azure location where the resource exists. Changing this forces a new resource to be created.

<h4 class="pdoc-member-header" id="PlacementGroup-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/759289fd9b3a0ab07d1ece84247638497d4bb8ba/sdk/nodejs/proximity/placementGroup.ts#L69">property <b>name</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>name: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Specifies the name of the availability set. Changing this forces a new resource to be created.

<h4 class="pdoc-member-header" id="PlacementGroup-resourceGroupName">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/759289fd9b3a0ab07d1ece84247638497d4bb8ba/sdk/nodejs/proximity/placementGroup.ts#L73">property <b>resourceGroupName</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>resourceGroupName: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The name of the resource group in which to create the availability set. Changing this forces a new resource to be created.

<h4 class="pdoc-member-header" id="PlacementGroup-tags">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/759289fd9b3a0ab07d1ece84247638497d4bb8ba/sdk/nodejs/proximity/placementGroup.ts#L77">property <b>tags</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>tags: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;{[key: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>]: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>} | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span>&gt;;</code></pre>

A mapping of tags to assign to the resource.

<h4 class="pdoc-member-header" id="PlacementGroup-urn">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/759289fd9b3a0ab07d1ece84247638497d4bb8ba/sdk/nodejs/proximity/placementGroup.ts#L34">property <b>urn</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>urn: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#URN'>URN</a>&gt;;</code></pre>

urn is the stable logical URN used to distinctly address a resource, both before and after
deployments.


<h2 id="functions">Functions</h2>
<h3 class="pdoc-module-header" id="getPlacementGroup" data-link-title="getPlacementGroup">
    <a href="https://github.com/pulumi/pulumi-azure/blob/759289fd9b3a0ab07d1ece84247638497d4bb8ba/sdk/nodejs/proximity/getPlacementGroup.ts#L24">
        Function <strong>getPlacementGroup</strong>
    </a>
</h3>


<pre class="highlight"><code><span class='kd'></span>getPlacementGroup(args: <a href='#GetPlacementGroupArgs'>GetPlacementGroupArgs</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions'>pulumi.InvokeOptions</a>): <a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise'>Promise</a>&lt;<a href='#GetPlacementGroupResult'>GetPlacementGroupResult</a>&gt;</code></pre>


Use this data source to access information about an existing Proximity Placement Group.

#### Example Usage

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as azure from "@pulumi/azure";

const example = azure.proximity.getPlacementGroup({
    name: "tf-appsecuritygroup",
    resourceGroupName: "my-resource-group",
});
export const proximityPlacementGroupId = example.then(example => example.id);
```


<h2 id="apis">Others</h2>
<h3 class="pdoc-module-header" id="GetPlacementGroupArgs" data-link-title="GetPlacementGroupArgs">
    <a href="https://github.com/pulumi/pulumi-azure/blob/759289fd9b3a0ab07d1ece84247638497d4bb8ba/sdk/nodejs/proximity/getPlacementGroup.ts#L41">
        interface <strong>GetPlacementGroupArgs</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>GetPlacementGroupArgs</span></code></pre>

A collection of arguments for invoking getPlacementGroup.

<h4 class="pdoc-member-header" id="GetPlacementGroupArgs-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/759289fd9b3a0ab07d1ece84247638497d4bb8ba/sdk/nodejs/proximity/getPlacementGroup.ts#L45">property <b>name</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>

The name of the Proximity Placement Group.

<h4 class="pdoc-member-header" id="GetPlacementGroupArgs-resourceGroupName">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/759289fd9b3a0ab07d1ece84247638497d4bb8ba/sdk/nodejs/proximity/getPlacementGroup.ts#L49">property <b>resourceGroupName</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>resourceGroupName: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>

The name of the resource group in which the Proximity Placement Group exists.

<h3 class="pdoc-module-header" id="GetPlacementGroupResult" data-link-title="GetPlacementGroupResult">
    <a href="https://github.com/pulumi/pulumi-azure/blob/759289fd9b3a0ab07d1ece84247638497d4bb8ba/sdk/nodejs/proximity/getPlacementGroup.ts#L55">
        interface <strong>GetPlacementGroupResult</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>GetPlacementGroupResult</span></code></pre>

A collection of values returned by getPlacementGroup.

<h4 class="pdoc-member-header" id="GetPlacementGroupResult-id">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/759289fd9b3a0ab07d1ece84247638497d4bb8ba/sdk/nodejs/proximity/getPlacementGroup.ts#L59">property <b>id</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>id: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>

The provider-assigned unique ID for this managed resource.

<h4 class="pdoc-member-header" id="GetPlacementGroupResult-location">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/759289fd9b3a0ab07d1ece84247638497d4bb8ba/sdk/nodejs/proximity/getPlacementGroup.ts#L60">property <b>location</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>location: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>
<h4 class="pdoc-member-header" id="GetPlacementGroupResult-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/759289fd9b3a0ab07d1ece84247638497d4bb8ba/sdk/nodejs/proximity/getPlacementGroup.ts#L61">property <b>name</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>
<h4 class="pdoc-member-header" id="GetPlacementGroupResult-resourceGroupName">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/759289fd9b3a0ab07d1ece84247638497d4bb8ba/sdk/nodejs/proximity/getPlacementGroup.ts#L62">property <b>resourceGroupName</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>resourceGroupName: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>
<h4 class="pdoc-member-header" id="GetPlacementGroupResult-tags">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/759289fd9b3a0ab07d1ece84247638497d4bb8ba/sdk/nodejs/proximity/getPlacementGroup.ts#L63">property <b>tags</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>tags: {[key: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>]: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>};</code></pre>
<h3 class="pdoc-module-header" id="PlacementGroupArgs" data-link-title="PlacementGroupArgs">
    <a href="https://github.com/pulumi/pulumi-azure/blob/759289fd9b3a0ab07d1ece84247638497d4bb8ba/sdk/nodejs/proximity/placementGroup.ts#L141">
        interface <strong>PlacementGroupArgs</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>PlacementGroupArgs</span></code></pre>

The set of arguments for constructing a PlacementGroup resource.

<h4 class="pdoc-member-header" id="PlacementGroupArgs-location">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/759289fd9b3a0ab07d1ece84247638497d4bb8ba/sdk/nodejs/proximity/placementGroup.ts#L145">property <b>location</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>location?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Specifies the supported Azure location where the resource exists. Changing this forces a new resource to be created.

<h4 class="pdoc-member-header" id="PlacementGroupArgs-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/759289fd9b3a0ab07d1ece84247638497d4bb8ba/sdk/nodejs/proximity/placementGroup.ts#L149">property <b>name</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>name?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Specifies the name of the availability set. Changing this forces a new resource to be created.

<h4 class="pdoc-member-header" id="PlacementGroupArgs-resourceGroupName">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/759289fd9b3a0ab07d1ece84247638497d4bb8ba/sdk/nodejs/proximity/placementGroup.ts#L153">property <b>resourceGroupName</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>resourceGroupName: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The name of the resource group in which to create the availability set. Changing this forces a new resource to be created.

<h4 class="pdoc-member-header" id="PlacementGroupArgs-tags">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/759289fd9b3a0ab07d1ece84247638497d4bb8ba/sdk/nodejs/proximity/placementGroup.ts#L157">property <b>tags</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>tags?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;{[key: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>]: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;}&gt;;</code></pre>

A mapping of tags to assign to the resource.

<h3 class="pdoc-module-header" id="PlacementGroupState" data-link-title="PlacementGroupState">
    <a href="https://github.com/pulumi/pulumi-azure/blob/759289fd9b3a0ab07d1ece84247638497d4bb8ba/sdk/nodejs/proximity/placementGroup.ts#L119">
        interface <strong>PlacementGroupState</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>PlacementGroupState</span></code></pre>

Input properties used for looking up and filtering PlacementGroup resources.

<h4 class="pdoc-member-header" id="PlacementGroupState-location">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/759289fd9b3a0ab07d1ece84247638497d4bb8ba/sdk/nodejs/proximity/placementGroup.ts#L123">property <b>location</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>location?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Specifies the supported Azure location where the resource exists. Changing this forces a new resource to be created.

<h4 class="pdoc-member-header" id="PlacementGroupState-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/759289fd9b3a0ab07d1ece84247638497d4bb8ba/sdk/nodejs/proximity/placementGroup.ts#L127">property <b>name</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>name?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Specifies the name of the availability set. Changing this forces a new resource to be created.

<h4 class="pdoc-member-header" id="PlacementGroupState-resourceGroupName">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/759289fd9b3a0ab07d1ece84247638497d4bb8ba/sdk/nodejs/proximity/placementGroup.ts#L131">property <b>resourceGroupName</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>resourceGroupName?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The name of the resource group in which to create the availability set. Changing this forces a new resource to be created.

<h4 class="pdoc-member-header" id="PlacementGroupState-tags">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/759289fd9b3a0ab07d1ece84247638497d4bb8ba/sdk/nodejs/proximity/placementGroup.ts#L135">property <b>tags</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>tags?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;{[key: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>]: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;}&gt;;</code></pre>

A mapping of tags to assign to the resource.

