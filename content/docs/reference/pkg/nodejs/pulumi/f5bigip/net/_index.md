---
title: "Module net"
title_tag: "Module net | Package @pulumi/f5bigip | Node.js SDK"
linktitle: "net"
meta_desc: "Explore members of the net module in the @pulumi/f5bigip package."
git_sha: "4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14"
block_external_search_index: true
---

<!-- WARNING: this page was generated by a tool. Do not edit it by hand. -->
<!-- To change it, please see https://github.com/pulumi/docs/tree/master/tools/tscdocgen. -->

{{< resource-docs-alert "f5bigip" >}}




<h3>Resources</h3>
<ul class="api">
    <li><a href="#Route"><span class="symbol resource"></span>Route</a></li>
    <li><a href="#SelfIp"><span class="symbol resource"></span>SelfIp</a></li>
    <li><a href="#Vlan"><span class="symbol resource"></span>Vlan</a></li>
</ul>


<h3>Others</h3>
<ul class="api">
    <li><a href="#RouteArgs"><span class="symbol api"></span>RouteArgs</a></li>
    <li><a href="#RouteState"><span class="symbol api"></span>RouteState</a></li>
    <li><a href="#SelfIpArgs"><span class="symbol api"></span>SelfIpArgs</a></li>
    <li><a href="#SelfIpState"><span class="symbol api"></span>SelfIpState</a></li>
    <li><a href="#VlanArgs"><span class="symbol api"></span>VlanArgs</a></li>
    <li><a href="#VlanState"><span class="symbol api"></span>VlanState</a></li>
</ul>


<h2 id="resources">Resources</h2>
<h3 class="pdoc-module-header" id="Route" data-link-title="Route">
    <a href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/route.ts#L25">
        Resource <strong>Route</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>class</span> <span class='nx'>Route</span> <span class='kr'>extends</span> <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResource'>CustomResource</a></code></pre>

`f5bigip.net.Route` Manages a route configuration

For resources should be named with their "full path". The full path is the combination of the partition + name of the resource. For example /Common/my-pool.

#### Example Usage

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as f5bigip from "@pulumi/f5bigip";

const route2 = new f5bigip.net.Route("route2", {
    gw: "1.1.1.2",
    name: "external-route",
    network: "10.10.10.0/24",
});
```

<h4 class="pdoc-member-header" id="Route-constructor">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/route.ts#L64"> <b>constructor</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span><span class='kd'>new</span> Route(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, args: <a href='#RouteArgs'>RouteArgs</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>)</code></pre>


Create a Route resource with the given unique name, arguments, and options.

* `name` The _unique_ name of the resource.
* `args` The arguments to use to populate this resource&#39;s properties.
* `opts` A bag of options that control this resource&#39;s behavior.

<h4 class="pdoc-member-header" id="Route-get">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/route.ts#L35">method <b>get</b></a>
</h4>


<pre class="highlight"><code><span class='kd'>public static </span>get(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>pulumi.ID</a>&gt;, state?: <a href='#RouteState'>RouteState</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>): <a href='#Route'>Route</a></code></pre>


Get an existing Route resource's state with the given name, ID, and optional extra
properties used to qualify the lookup.

<h4 class="pdoc-member-header" id="Route-getProvider">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/route.ts#L25">method <b>getProvider</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>getProvider(moduleMember: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>): <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ProviderResource'>ProviderResource</a> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span></code></pre>

<h4 class="pdoc-member-header" id="Route-isInstance">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/route.ts#L46">method <b>isInstance</b></a>
</h4>


<pre class="highlight"><code><span class='kd'>public static </span>isInstance(obj: <span class='kd'><a href='https://www.typescriptlang.org/docs/handbook/basic-types.html#any'>any</a></span>): obj is Route</code></pre>


Returns true if the given object is an instance of Route.  This is designed to work even
when multiple copies of the Pulumi SDK have been loaded into the same process.

<h4 class="pdoc-member-header" id="Route-gw">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/route.ts#L56">property <b>gw</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>gw: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span>&gt;;</code></pre>

Specifies a gateway address for the route.

<h4 class="pdoc-member-header" id="Route-id">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/route.ts#L25">property <b>id</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>ID</a>&gt;;</code></pre>

id is the provider-assigned unique ID for this managed resource.  It is set during
deployments and may be missing (undefined) during planning phases.

<h4 class="pdoc-member-header" id="Route-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/route.ts#L60">property <b>name</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>name: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Name of the route

<h4 class="pdoc-member-header" id="Route-network">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/route.ts#L64">property <b>network</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>network: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The destination subnet and netmask for the route.

<h4 class="pdoc-member-header" id="Route-urn">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/route.ts#L25">property <b>urn</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>urn: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#URN'>URN</a>&gt;;</code></pre>

urn is the stable logical URN used to distinctly address a resource, both before and after
deployments.

<h3 class="pdoc-module-header" id="SelfIp" data-link-title="SelfIp">
    <a href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/selfIp.ts#L28">
        Resource <strong>SelfIp</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>class</span> <span class='nx'>SelfIp</span> <span class='kr'>extends</span> <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResource'>CustomResource</a></code></pre>

`f5bigip.net.SelfIp` Manages a selfip configuration

Resource should be named with their "full path". The full path is the combination of the partition + name of the resource, for example /Common/my-selfip.

#### Example Usage

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as f5bigip from "@pulumi/f5bigip";

const selfip1 = new f5bigip.net.SelfIp("selfip1", {
    name: "/Common/internalselfIP",
    ip: "11.1.1.1/24",
    vlan: "/Common/internal",
    trafficGroup: "traffic-group-1",
}, {
    dependsOn: [bigip_net_vlan.vlan1],
});
```

<h4 class="pdoc-member-header" id="SelfIp-constructor">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/selfIp.ts#L71"> <b>constructor</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span><span class='kd'>new</span> SelfIp(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, args: <a href='#SelfIpArgs'>SelfIpArgs</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>)</code></pre>


Create a SelfIp resource with the given unique name, arguments, and options.

* `name` The _unique_ name of the resource.
* `args` The arguments to use to populate this resource&#39;s properties.
* `opts` A bag of options that control this resource&#39;s behavior.

<h4 class="pdoc-member-header" id="SelfIp-get">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/selfIp.ts#L38">method <b>get</b></a>
</h4>


<pre class="highlight"><code><span class='kd'>public static </span>get(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>pulumi.ID</a>&gt;, state?: <a href='#SelfIpState'>SelfIpState</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>): <a href='#SelfIp'>SelfIp</a></code></pre>


Get an existing SelfIp resource's state with the given name, ID, and optional extra
properties used to qualify the lookup.

<h4 class="pdoc-member-header" id="SelfIp-getProvider">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/selfIp.ts#L28">method <b>getProvider</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>getProvider(moduleMember: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>): <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ProviderResource'>ProviderResource</a> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span></code></pre>

<h4 class="pdoc-member-header" id="SelfIp-isInstance">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/selfIp.ts#L49">method <b>isInstance</b></a>
</h4>


<pre class="highlight"><code><span class='kd'>public static </span>isInstance(obj: <span class='kd'><a href='https://www.typescriptlang.org/docs/handbook/basic-types.html#any'>any</a></span>): obj is SelfIp</code></pre>


Returns true if the given object is an instance of SelfIp.  This is designed to work even
when multiple copies of the Pulumi SDK have been loaded into the same process.

<h4 class="pdoc-member-header" id="SelfIp-id">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/selfIp.ts#L28">property <b>id</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>ID</a>&gt;;</code></pre>

id is the provider-assigned unique ID for this managed resource.  It is set during
deployments and may be missing (undefined) during planning phases.

<h4 class="pdoc-member-header" id="SelfIp-ip">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/selfIp.ts#L59">property <b>ip</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>ip: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The Self IP's address and netmask.

<h4 class="pdoc-member-header" id="SelfIp-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/selfIp.ts#L63">property <b>name</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>name: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Name of the selfip

<h4 class="pdoc-member-header" id="SelfIp-trafficGroup">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/selfIp.ts#L67">property <b>trafficGroup</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>trafficGroup: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span>&gt;;</code></pre>

Specifies the traffic group, defaults to `traffic-group-local-only` if not specified.

<h4 class="pdoc-member-header" id="SelfIp-urn">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/selfIp.ts#L28">property <b>urn</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>urn: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#URN'>URN</a>&gt;;</code></pre>

urn is the stable logical URN used to distinctly address a resource, both before and after
deployments.

<h4 class="pdoc-member-header" id="SelfIp-vlan">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/selfIp.ts#L71">property <b>vlan</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>vlan: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Specifies the VLAN for which you are setting a self IP address. This setting must be provided when a self IP is created.

<h3 class="pdoc-module-header" id="Vlan" data-link-title="Vlan">
    <a href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/vlan.ts#L29">
        Resource <strong>Vlan</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>class</span> <span class='nx'>Vlan</span> <span class='kr'>extends</span> <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResource'>CustomResource</a></code></pre>

`f5bigip.net.Vlan` Manages a vlan configuration

For resources should be named with their "full path". The full path is the combination of the partition + name of the resource. For example /Common/my-pool.

#### Example Usage

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as f5bigip from "@pulumi/f5bigip";

const vlan1 = new f5bigip.net.Vlan("vlan1", {
    interfaces: [{
        tagged: false,
        vlanport: "1.2",
    }],
    name: "/Common/Internal",
    tag: 101,
});
```

<h4 class="pdoc-member-header" id="Vlan-constructor">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/vlan.ts#L68"> <b>constructor</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span><span class='kd'>new</span> Vlan(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, args: <a href='#VlanArgs'>VlanArgs</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>)</code></pre>


Create a Vlan resource with the given unique name, arguments, and options.

* `name` The _unique_ name of the resource.
* `args` The arguments to use to populate this resource&#39;s properties.
* `opts` A bag of options that control this resource&#39;s behavior.

<h4 class="pdoc-member-header" id="Vlan-get">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/vlan.ts#L39">method <b>get</b></a>
</h4>


<pre class="highlight"><code><span class='kd'>public static </span>get(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>pulumi.ID</a>&gt;, state?: <a href='#VlanState'>VlanState</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>): <a href='#Vlan'>Vlan</a></code></pre>


Get an existing Vlan resource's state with the given name, ID, and optional extra
properties used to qualify the lookup.

<h4 class="pdoc-member-header" id="Vlan-getProvider">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/vlan.ts#L29">method <b>getProvider</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>getProvider(moduleMember: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>): <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ProviderResource'>ProviderResource</a> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span></code></pre>

<h4 class="pdoc-member-header" id="Vlan-isInstance">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/vlan.ts#L50">method <b>isInstance</b></a>
</h4>


<pre class="highlight"><code><span class='kd'>public static </span>isInstance(obj: <span class='kd'><a href='https://www.typescriptlang.org/docs/handbook/basic-types.html#any'>any</a></span>): obj is Vlan</code></pre>


Returns true if the given object is an instance of Vlan.  This is designed to work even
when multiple copies of the Pulumi SDK have been loaded into the same process.

<h4 class="pdoc-member-header" id="Vlan-id">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/vlan.ts#L29">property <b>id</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>ID</a>&gt;;</code></pre>

id is the provider-assigned unique ID for this managed resource.  It is set during
deployments and may be missing (undefined) during planning phases.

<h4 class="pdoc-member-header" id="Vlan-interfaces">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/vlan.ts#L60">property <b>interfaces</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>interfaces: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/f5bigip/types/output/#VlanInterface'>VlanInterface</a>[] | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span>&gt;;</code></pre>

Specifies which interfaces you want this VLAN to use for traffic management.

<h4 class="pdoc-member-header" id="Vlan-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/vlan.ts#L64">property <b>name</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>name: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Name of the vlan

<h4 class="pdoc-member-header" id="Vlan-tag">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/vlan.ts#L68">property <b>tag</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>tag: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number'>number</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span>&gt;;</code></pre>

Specifies a number that the system adds into the header of any frame passing through the VLAN.

<h4 class="pdoc-member-header" id="Vlan-urn">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/vlan.ts#L29">property <b>urn</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>urn: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#URN'>URN</a>&gt;;</code></pre>

urn is the stable logical URN used to distinctly address a resource, both before and after
deployments.



<h2 id="apis">Others</h2>
<h3 class="pdoc-module-header" id="RouteArgs" data-link-title="RouteArgs">
    <a href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/route.ts#L125">
        interface <strong>RouteArgs</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>RouteArgs</span></code></pre>

The set of arguments for constructing a Route resource.

<h4 class="pdoc-member-header" id="RouteArgs-gw">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/route.ts#L129">property <b>gw</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>gw?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Specifies a gateway address for the route.

<h4 class="pdoc-member-header" id="RouteArgs-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/route.ts#L133">property <b>name</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>name: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Name of the route

<h4 class="pdoc-member-header" id="RouteArgs-network">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/route.ts#L137">property <b>network</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>network: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The destination subnet and netmask for the route.

<h3 class="pdoc-module-header" id="RouteState" data-link-title="RouteState">
    <a href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/route.ts#L107">
        interface <strong>RouteState</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>RouteState</span></code></pre>

Input properties used for looking up and filtering Route resources.

<h4 class="pdoc-member-header" id="RouteState-gw">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/route.ts#L111">property <b>gw</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>gw?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Specifies a gateway address for the route.

<h4 class="pdoc-member-header" id="RouteState-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/route.ts#L115">property <b>name</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>name?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Name of the route

<h4 class="pdoc-member-header" id="RouteState-network">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/route.ts#L119">property <b>network</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>network?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The destination subnet and netmask for the route.

<h3 class="pdoc-module-header" id="SelfIpArgs" data-link-title="SelfIpArgs">
    <a href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/selfIp.ts#L141">
        interface <strong>SelfIpArgs</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>SelfIpArgs</span></code></pre>

The set of arguments for constructing a SelfIp resource.

<h4 class="pdoc-member-header" id="SelfIpArgs-ip">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/selfIp.ts#L145">property <b>ip</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>ip: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The Self IP's address and netmask.

<h4 class="pdoc-member-header" id="SelfIpArgs-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/selfIp.ts#L149">property <b>name</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>name: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Name of the selfip

<h4 class="pdoc-member-header" id="SelfIpArgs-trafficGroup">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/selfIp.ts#L153">property <b>trafficGroup</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>trafficGroup?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Specifies the traffic group, defaults to `traffic-group-local-only` if not specified.

<h4 class="pdoc-member-header" id="SelfIpArgs-vlan">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/selfIp.ts#L157">property <b>vlan</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>vlan: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Specifies the VLAN for which you are setting a self IP address. This setting must be provided when a self IP is created.

<h3 class="pdoc-module-header" id="SelfIpState" data-link-title="SelfIpState">
    <a href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/selfIp.ts#L119">
        interface <strong>SelfIpState</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>SelfIpState</span></code></pre>

Input properties used for looking up and filtering SelfIp resources.

<h4 class="pdoc-member-header" id="SelfIpState-ip">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/selfIp.ts#L123">property <b>ip</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>ip?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The Self IP's address and netmask.

<h4 class="pdoc-member-header" id="SelfIpState-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/selfIp.ts#L127">property <b>name</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>name?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Name of the selfip

<h4 class="pdoc-member-header" id="SelfIpState-trafficGroup">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/selfIp.ts#L131">property <b>trafficGroup</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>trafficGroup?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Specifies the traffic group, defaults to `traffic-group-local-only` if not specified.

<h4 class="pdoc-member-header" id="SelfIpState-vlan">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/selfIp.ts#L135">property <b>vlan</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>vlan?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Specifies the VLAN for which you are setting a self IP address. This setting must be provided when a self IP is created.

<h3 class="pdoc-module-header" id="VlanArgs" data-link-title="VlanArgs">
    <a href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/vlan.ts#L126">
        interface <strong>VlanArgs</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>VlanArgs</span></code></pre>

The set of arguments for constructing a Vlan resource.

<h4 class="pdoc-member-header" id="VlanArgs-interfaces">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/vlan.ts#L130">property <b>interfaces</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>interfaces?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/f5bigip/types/input/#VlanInterface'>VlanInterface</a>&gt;[]&gt;;</code></pre>

Specifies which interfaces you want this VLAN to use for traffic management.

<h4 class="pdoc-member-header" id="VlanArgs-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/vlan.ts#L134">property <b>name</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>name: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Name of the vlan

<h4 class="pdoc-member-header" id="VlanArgs-tag">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/vlan.ts#L138">property <b>tag</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>tag?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number'>number</a></span>&gt;;</code></pre>

Specifies a number that the system adds into the header of any frame passing through the VLAN.

<h3 class="pdoc-module-header" id="VlanState" data-link-title="VlanState">
    <a href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/vlan.ts#L108">
        interface <strong>VlanState</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>VlanState</span></code></pre>

Input properties used for looking up and filtering Vlan resources.

<h4 class="pdoc-member-header" id="VlanState-interfaces">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/vlan.ts#L112">property <b>interfaces</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>interfaces?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/f5bigip/types/input/#VlanInterface'>VlanInterface</a>&gt;[]&gt;;</code></pre>

Specifies which interfaces you want this VLAN to use for traffic management.

<h4 class="pdoc-member-header" id="VlanState-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/vlan.ts#L116">property <b>name</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>name?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Name of the vlan

<h4 class="pdoc-member-header" id="VlanState-tag">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/net/vlan.ts#L120">property <b>tag</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>tag?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number'>number</a></span>&gt;;</code></pre>

Specifies a number that the system adds into the header of any frame passing through the VLAN.

