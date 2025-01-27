---
title: "Module outposts"
title_tag: "Module outposts | Package @pulumi/aws | Node.js SDK"
linktitle: "outposts"
meta_desc: "Explore members of the outposts module in the @pulumi/aws package."
git_sha: "6c9e985f93682e9b4056b497c1a31a75fd7884fc"
block_external_search_index: true
---

<!-- WARNING: this page was generated by a tool. Do not edit it by hand. -->
<!-- To change it, please see https://github.com/pulumi/docs/tree/master/tools/tscdocgen. -->

{{< resource-docs-alert "aws" >}}





<h3>Functions</h3>
<ul class="api">
    <li><a href="#getOutpost"><span class="symbol function"></span>getOutpost</a></li>
    <li><a href="#getOutpostInstanceType"><span class="symbol function"></span>getOutpostInstanceType</a></li>
    <li><a href="#getOutpostInstanceTypes"><span class="symbol function"></span>getOutpostInstanceTypes</a></li>
    <li><a href="#getOutposts"><span class="symbol function"></span>getOutposts</a></li>
    <li><a href="#getSite"><span class="symbol function"></span>getSite</a></li>
    <li><a href="#getSites"><span class="symbol function"></span>getSites</a></li>
</ul>

<h3>Others</h3>
<ul class="api">
    <li><a href="#GetOutpostArgs"><span class="symbol api"></span>GetOutpostArgs</a></li>
    <li><a href="#GetOutpostInstanceTypeArgs"><span class="symbol api"></span>GetOutpostInstanceTypeArgs</a></li>
    <li><a href="#GetOutpostInstanceTypeResult"><span class="symbol api"></span>GetOutpostInstanceTypeResult</a></li>
    <li><a href="#GetOutpostInstanceTypesArgs"><span class="symbol api"></span>GetOutpostInstanceTypesArgs</a></li>
    <li><a href="#GetOutpostInstanceTypesResult"><span class="symbol api"></span>GetOutpostInstanceTypesResult</a></li>
    <li><a href="#GetOutpostResult"><span class="symbol api"></span>GetOutpostResult</a></li>
    <li><a href="#GetOutpostsArgs"><span class="symbol api"></span>GetOutpostsArgs</a></li>
    <li><a href="#GetOutpostsResult"><span class="symbol api"></span>GetOutpostsResult</a></li>
    <li><a href="#GetSiteArgs"><span class="symbol api"></span>GetSiteArgs</a></li>
    <li><a href="#GetSiteResult"><span class="symbol api"></span>GetSiteResult</a></li>
    <li><a href="#GetSitesResult"><span class="symbol api"></span>GetSitesResult</a></li>
</ul>



<h2 id="functions">Functions</h2>
<h3 class="pdoc-module-header" id="getOutpost" data-link-title="getOutpost">
    <a href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getOutpost.ts#L22">
        Function <strong>getOutpost</strong>
    </a>
</h3>


<pre class="highlight"><code><span class='kd'></span>getOutpost(args?: <a href='#GetOutpostArgs'>GetOutpostArgs</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions'>pulumi.InvokeOptions</a>): <a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise'>Promise</a>&lt;<a href='#GetOutpostResult'>GetOutpostResult</a>&gt;</code></pre>


Provides details about an Outposts Outpost.

#### Example Usage

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws from "@pulumi/aws";

const example = pulumi.output(aws.outposts.getOutpost({
    name: "example",
}, { async: true }));
```

<h3 class="pdoc-module-header" id="getOutpostInstanceType" data-link-title="getOutpostInstanceType">
    <a href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getOutpostInstanceType.ts#L11">
        Function <strong>getOutpostInstanceType</strong>
    </a>
</h3>


<pre class="highlight"><code><span class='kd'></span>getOutpostInstanceType(args: <a href='#GetOutpostInstanceTypeArgs'>GetOutpostInstanceTypeArgs</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions'>pulumi.InvokeOptions</a>): <a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise'>Promise</a>&lt;<a href='#GetOutpostInstanceTypeResult'>GetOutpostInstanceTypeResult</a>&gt;</code></pre>


Information about single Outpost Instance Type.

<h3 class="pdoc-module-header" id="getOutpostInstanceTypes" data-link-title="getOutpostInstanceTypes">
    <a href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getOutpostInstanceTypes.ts#L22">
        Function <strong>getOutpostInstanceTypes</strong>
    </a>
</h3>


<pre class="highlight"><code><span class='kd'></span>getOutpostInstanceTypes(args: <a href='#GetOutpostInstanceTypesArgs'>GetOutpostInstanceTypesArgs</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions'>pulumi.InvokeOptions</a>): <a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise'>Promise</a>&lt;<a href='#GetOutpostInstanceTypesResult'>GetOutpostInstanceTypesResult</a>&gt;</code></pre>


Information about Outposts Instance Types.

#### Example Usage

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws from "@pulumi/aws";

const example = aws.outposts.getOutpostInstanceTypes({
    arn: data.aws_outposts_outpost.example.arn,
});
```

<h3 class="pdoc-module-header" id="getOutposts" data-link-title="getOutposts">
    <a href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getOutposts.ts#L22">
        Function <strong>getOutposts</strong>
    </a>
</h3>


<pre class="highlight"><code><span class='kd'></span>getOutposts(args?: <a href='#GetOutpostsArgs'>GetOutpostsArgs</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions'>pulumi.InvokeOptions</a>): <a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise'>Promise</a>&lt;<a href='#GetOutpostsResult'>GetOutpostsResult</a>&gt;</code></pre>


Provides details about multiple Outposts.

#### Example Usage

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws from "@pulumi/aws";

const example = aws.outposts.getOutposts({
    siteId: data.aws_outposts_site.id,
});
```

<h3 class="pdoc-module-header" id="getSite" data-link-title="getSite">
    <a href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getSite.ts#L22">
        Function <strong>getSite</strong>
    </a>
</h3>


<pre class="highlight"><code><span class='kd'></span>getSite(args?: <a href='#GetSiteArgs'>GetSiteArgs</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions'>pulumi.InvokeOptions</a>): <a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise'>Promise</a>&lt;<a href='#GetSiteResult'>GetSiteResult</a>&gt;</code></pre>


Provides details about an Outposts Site.

#### Example Usage

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws from "@pulumi/aws";

const example = pulumi.output(aws.outposts.getSite({
    name: "example",
}, { async: true }));
```

<h3 class="pdoc-module-header" id="getSites" data-link-title="getSites">
    <a href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getSites.ts#L20">
        Function <strong>getSites</strong>
    </a>
</h3>


<pre class="highlight"><code><span class='kd'></span>getSites(opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions'>pulumi.InvokeOptions</a>): <a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise'>Promise</a>&lt;<a href='#GetSitesResult'>GetSitesResult</a>&gt;</code></pre>


Provides details about multiple Outposts Sites.

#### Example Usage

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws from "@pulumi/aws";

const all = pulumi.output(aws.outposts.getSites({ async: true }));
```


<h2 id="apis">Others</h2>
<h3 class="pdoc-module-header" id="GetOutpostArgs" data-link-title="GetOutpostArgs">
    <a href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getOutpost.ts#L41">
        interface <strong>GetOutpostArgs</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>GetOutpostArgs</span></code></pre>

A collection of arguments for invoking getOutpost.

<h4 class="pdoc-member-header" id="GetOutpostArgs-arn">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getOutpost.ts#L45">property <b>arn</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>arn?: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>

Amazon Resource Name (ARN).

<h4 class="pdoc-member-header" id="GetOutpostArgs-id">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getOutpost.ts#L49">property <b>id</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>id?: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>

Identifier of the Outpost.

<h4 class="pdoc-member-header" id="GetOutpostArgs-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getOutpost.ts#L53">property <b>name</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>name?: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>

Name of the Outpost.

<h3 class="pdoc-module-header" id="GetOutpostInstanceTypeArgs" data-link-title="GetOutpostInstanceTypeArgs">
    <a href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getOutpostInstanceType.ts#L29">
        interface <strong>GetOutpostInstanceTypeArgs</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>GetOutpostInstanceTypeArgs</span></code></pre>

A collection of arguments for invoking getOutpostInstanceType.

<h4 class="pdoc-member-header" id="GetOutpostInstanceTypeArgs-arn">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getOutpostInstanceType.ts#L33">property <b>arn</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>arn: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>

Outpost Amazon Resource Name (ARN).

<h4 class="pdoc-member-header" id="GetOutpostInstanceTypeArgs-instanceType">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getOutpostInstanceType.ts#L37">property <b>instanceType</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>instanceType?: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>

Desired instance type. Conflicts with `preferredInstanceTypes`.

<h4 class="pdoc-member-header" id="GetOutpostInstanceTypeArgs-preferredInstanceTypes">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getOutpostInstanceType.ts#L41">property <b>preferredInstanceTypes</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>preferredInstanceTypes?: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>[];</code></pre>

Ordered list of preferred instance types. The first match in this list will be returned. If no preferred matches are found and the original search returned more than one result, an error is returned. Conflicts with `instanceType`.

<h3 class="pdoc-module-header" id="GetOutpostInstanceTypeResult" data-link-title="GetOutpostInstanceTypeResult">
    <a href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getOutpostInstanceType.ts#L47">
        interface <strong>GetOutpostInstanceTypeResult</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>GetOutpostInstanceTypeResult</span></code></pre>

A collection of values returned by getOutpostInstanceType.

<h4 class="pdoc-member-header" id="GetOutpostInstanceTypeResult-arn">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getOutpostInstanceType.ts#L48">property <b>arn</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>arn: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>
<h4 class="pdoc-member-header" id="GetOutpostInstanceTypeResult-id">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getOutpostInstanceType.ts#L52">property <b>id</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>id: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>

The provider-assigned unique ID for this managed resource.

<h4 class="pdoc-member-header" id="GetOutpostInstanceTypeResult-instanceType">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getOutpostInstanceType.ts#L53">property <b>instanceType</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>instanceType: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>
<h4 class="pdoc-member-header" id="GetOutpostInstanceTypeResult-preferredInstanceTypes">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getOutpostInstanceType.ts#L54">property <b>preferredInstanceTypes</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>preferredInstanceTypes?: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>[];</code></pre>
<h3 class="pdoc-module-header" id="GetOutpostInstanceTypesArgs" data-link-title="GetOutpostInstanceTypesArgs">
    <a href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getOutpostInstanceTypes.ts#L38">
        interface <strong>GetOutpostInstanceTypesArgs</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>GetOutpostInstanceTypesArgs</span></code></pre>

A collection of arguments for invoking getOutpostInstanceTypes.

<h4 class="pdoc-member-header" id="GetOutpostInstanceTypesArgs-arn">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getOutpostInstanceTypes.ts#L42">property <b>arn</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>arn: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>

Outpost Amazon Resource Name (ARN).

<h3 class="pdoc-module-header" id="GetOutpostInstanceTypesResult" data-link-title="GetOutpostInstanceTypesResult">
    <a href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getOutpostInstanceTypes.ts#L48">
        interface <strong>GetOutpostInstanceTypesResult</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>GetOutpostInstanceTypesResult</span></code></pre>

A collection of values returned by getOutpostInstanceTypes.

<h4 class="pdoc-member-header" id="GetOutpostInstanceTypesResult-arn">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getOutpostInstanceTypes.ts#L49">property <b>arn</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>arn: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>
<h4 class="pdoc-member-header" id="GetOutpostInstanceTypesResult-id">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getOutpostInstanceTypes.ts#L53">property <b>id</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>id: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>

The provider-assigned unique ID for this managed resource.

<h4 class="pdoc-member-header" id="GetOutpostInstanceTypesResult-instanceTypes">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getOutpostInstanceTypes.ts#L57">property <b>instanceTypes</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>instanceTypes: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>[];</code></pre>

Set of instance types.

<h3 class="pdoc-module-header" id="GetOutpostResult" data-link-title="GetOutpostResult">
    <a href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getOutpost.ts#L59">
        interface <strong>GetOutpostResult</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>GetOutpostResult</span></code></pre>

A collection of values returned by getOutpost.

<h4 class="pdoc-member-header" id="GetOutpostResult-arn">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getOutpost.ts#L60">property <b>arn</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>arn: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>
<h4 class="pdoc-member-header" id="GetOutpostResult-availabilityZone">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getOutpost.ts#L64">property <b>availabilityZone</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>availabilityZone: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>

Availability Zone name.

<h4 class="pdoc-member-header" id="GetOutpostResult-availabilityZoneId">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getOutpost.ts#L68">property <b>availabilityZoneId</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>availabilityZoneId: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>

Availability Zone identifier.

<h4 class="pdoc-member-header" id="GetOutpostResult-description">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getOutpost.ts#L72">property <b>description</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>description: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>

Description.

<h4 class="pdoc-member-header" id="GetOutpostResult-id">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getOutpost.ts#L73">property <b>id</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>id: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>
<h4 class="pdoc-member-header" id="GetOutpostResult-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getOutpost.ts#L74">property <b>name</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>
<h4 class="pdoc-member-header" id="GetOutpostResult-ownerId">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getOutpost.ts#L78">property <b>ownerId</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>ownerId: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>

AWS Account identifier of the Outpost owner.

<h4 class="pdoc-member-header" id="GetOutpostResult-siteId">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getOutpost.ts#L82">property <b>siteId</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>siteId: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>

Site identifier.

<h3 class="pdoc-module-header" id="GetOutpostsArgs" data-link-title="GetOutpostsArgs">
    <a href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getOutposts.ts#L41">
        interface <strong>GetOutpostsArgs</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>GetOutpostsArgs</span></code></pre>

A collection of arguments for invoking getOutposts.

<h4 class="pdoc-member-header" id="GetOutpostsArgs-availabilityZone">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getOutposts.ts#L45">property <b>availabilityZone</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>availabilityZone?: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>

Availability Zone name.

<h4 class="pdoc-member-header" id="GetOutpostsArgs-availabilityZoneId">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getOutposts.ts#L49">property <b>availabilityZoneId</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>availabilityZoneId?: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>

Availability Zone identifier.

<h4 class="pdoc-member-header" id="GetOutpostsArgs-siteId">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getOutposts.ts#L53">property <b>siteId</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>siteId?: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>

Site identifier.

<h3 class="pdoc-module-header" id="GetOutpostsResult" data-link-title="GetOutpostsResult">
    <a href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getOutposts.ts#L59">
        interface <strong>GetOutpostsResult</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>GetOutpostsResult</span></code></pre>

A collection of values returned by getOutposts.

<h4 class="pdoc-member-header" id="GetOutpostsResult-arns">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getOutposts.ts#L63">property <b>arns</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>arns: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>[];</code></pre>

Set of Amazon Resource Names (ARNs).

<h4 class="pdoc-member-header" id="GetOutpostsResult-availabilityZone">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getOutposts.ts#L64">property <b>availabilityZone</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>availabilityZone: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>
<h4 class="pdoc-member-header" id="GetOutpostsResult-availabilityZoneId">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getOutposts.ts#L65">property <b>availabilityZoneId</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>availabilityZoneId: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>
<h4 class="pdoc-member-header" id="GetOutpostsResult-id">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getOutposts.ts#L69">property <b>id</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>id: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>

The provider-assigned unique ID for this managed resource.

<h4 class="pdoc-member-header" id="GetOutpostsResult-ids">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getOutposts.ts#L73">property <b>ids</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>ids: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>[];</code></pre>

Set of identifiers.

<h4 class="pdoc-member-header" id="GetOutpostsResult-siteId">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getOutposts.ts#L74">property <b>siteId</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>siteId: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>
<h3 class="pdoc-module-header" id="GetSiteArgs" data-link-title="GetSiteArgs">
    <a href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getSite.ts#L40">
        interface <strong>GetSiteArgs</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>GetSiteArgs</span></code></pre>

A collection of arguments for invoking getSite.

<h4 class="pdoc-member-header" id="GetSiteArgs-id">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getSite.ts#L44">property <b>id</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>id?: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>

Identifier of the Site.

<h4 class="pdoc-member-header" id="GetSiteArgs-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getSite.ts#L48">property <b>name</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>name?: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>

Name of the Site.

<h3 class="pdoc-module-header" id="GetSiteResult" data-link-title="GetSiteResult">
    <a href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getSite.ts#L54">
        interface <strong>GetSiteResult</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>GetSiteResult</span></code></pre>

A collection of values returned by getSite.

<h4 class="pdoc-member-header" id="GetSiteResult-accountId">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getSite.ts#L58">property <b>accountId</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>accountId: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>

AWS Account identifier.

<h4 class="pdoc-member-header" id="GetSiteResult-description">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getSite.ts#L62">property <b>description</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>description: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>

Description.

<h4 class="pdoc-member-header" id="GetSiteResult-id">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getSite.ts#L63">property <b>id</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>id: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>
<h4 class="pdoc-member-header" id="GetSiteResult-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getSite.ts#L64">property <b>name</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>
<h3 class="pdoc-module-header" id="GetSitesResult" data-link-title="GetSitesResult">
    <a href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getSites.ts#L35">
        interface <strong>GetSitesResult</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>GetSitesResult</span></code></pre>

A collection of values returned by getSites.

<h4 class="pdoc-member-header" id="GetSitesResult-id">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getSites.ts#L39">property <b>id</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>id: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>

The provider-assigned unique ID for this managed resource.

<h4 class="pdoc-member-header" id="GetSitesResult-ids">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/outposts/getSites.ts#L43">property <b>ids</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>ids: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>[];</code></pre>

Set of Outposts Site identifiers.

