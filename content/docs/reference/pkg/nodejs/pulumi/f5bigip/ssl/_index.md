---
title: "Module ssl"
title_tag: "Module ssl | Package @pulumi/f5bigip | Node.js SDK"
linktitle: "ssl"
meta_desc: "Explore members of the ssl module in the @pulumi/f5bigip package."
git_sha: "4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14"
block_external_search_index: true
---

<!-- WARNING: this page was generated by a tool. Do not edit it by hand. -->
<!-- To change it, please see https://github.com/pulumi/docs/tree/master/tools/tscdocgen. -->

{{< resource-docs-alert "f5bigip" >}}




<h3>Resources</h3>
<ul class="api">
    <li><a href="#Certificate"><span class="symbol resource"></span>Certificate</a></li>
    <li><a href="#Key"><span class="symbol resource"></span>Key</a></li>
</ul>

<h3>Functions</h3>
<ul class="api">
    <li><a href="#getCertificate"><span class="symbol function"></span>getCertificate</a></li>
</ul>

<h3>Others</h3>
<ul class="api">
    <li><a href="#CertificateArgs"><span class="symbol api"></span>CertificateArgs</a></li>
    <li><a href="#CertificateState"><span class="symbol api"></span>CertificateState</a></li>
    <li><a href="#GetCertificateArgs"><span class="symbol api"></span>GetCertificateArgs</a></li>
    <li><a href="#GetCertificateResult"><span class="symbol api"></span>GetCertificateResult</a></li>
    <li><a href="#KeyArgs"><span class="symbol api"></span>KeyArgs</a></li>
    <li><a href="#KeyState"><span class="symbol api"></span>KeyState</a></li>
</ul>


<h2 id="resources">Resources</h2>
<h3 class="pdoc-module-header" id="Certificate" data-link-title="Certificate">
    <a href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/ssl/certificate.ts#L25">
        Resource <strong>Certificate</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>class</span> <span class='nx'>Certificate</span> <span class='kr'>extends</span> <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResource'>CustomResource</a></code></pre>

`f5bigip.ssl.Certificate` This resource will import SSL certificates on BIG-IP LTM.
Certificates can be imported from certificate files on the local disk, in PEM format

#### Example Usage

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as f5bigip from "@pulumi/f5bigip";
import * from "fs";

const test_cert = new f5bigip.ssl.Certificate("test-cert", {
    name: "servercert.crt",
    content: fs.readFileSync("servercert.crt"),
    partition: "Common",
});
```

<h4 class="pdoc-member-header" id="Certificate-constructor">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/ssl/certificate.ts#L64"> <b>constructor</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span><span class='kd'>new</span> Certificate(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, args: <a href='#CertificateArgs'>CertificateArgs</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>)</code></pre>


Create a Certificate resource with the given unique name, arguments, and options.

* `name` The _unique_ name of the resource.
* `args` The arguments to use to populate this resource&#39;s properties.
* `opts` A bag of options that control this resource&#39;s behavior.

<h4 class="pdoc-member-header" id="Certificate-get">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/ssl/certificate.ts#L35">method <b>get</b></a>
</h4>


<pre class="highlight"><code><span class='kd'>public static </span>get(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>pulumi.ID</a>&gt;, state?: <a href='#CertificateState'>CertificateState</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>): <a href='#Certificate'>Certificate</a></code></pre>


Get an existing Certificate resource's state with the given name, ID, and optional extra
properties used to qualify the lookup.

<h4 class="pdoc-member-header" id="Certificate-getProvider">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/ssl/certificate.ts#L25">method <b>getProvider</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>getProvider(moduleMember: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>): <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ProviderResource'>ProviderResource</a> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span></code></pre>

<h4 class="pdoc-member-header" id="Certificate-isInstance">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/ssl/certificate.ts#L46">method <b>isInstance</b></a>
</h4>


<pre class="highlight"><code><span class='kd'>public static </span>isInstance(obj: <span class='kd'><a href='https://www.typescriptlang.org/docs/handbook/basic-types.html#any'>any</a></span>): obj is Certificate</code></pre>


Returns true if the given object is an instance of Certificate.  This is designed to work even
when multiple copies of the Pulumi SDK have been loaded into the same process.

<h4 class="pdoc-member-header" id="Certificate-content">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/ssl/certificate.ts#L56">property <b>content</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>content: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Content of certificate on Disk

<h4 class="pdoc-member-header" id="Certificate-id">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/ssl/certificate.ts#L25">property <b>id</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>ID</a>&gt;;</code></pre>

id is the provider-assigned unique ID for this managed resource.  It is set during
deployments and may be missing (undefined) during planning phases.

<h4 class="pdoc-member-header" id="Certificate-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/ssl/certificate.ts#L60">property <b>name</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>name: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Name of the SSL Certificate to be Imported on to BIGIP

<h4 class="pdoc-member-header" id="Certificate-partition">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/ssl/certificate.ts#L64">property <b>partition</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>partition: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span>&gt;;</code></pre>

Partition on to SSL Certificate to be imported

<h4 class="pdoc-member-header" id="Certificate-urn">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/ssl/certificate.ts#L25">property <b>urn</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>urn: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#URN'>URN</a>&gt;;</code></pre>

urn is the stable logical URN used to distinctly address a resource, both before and after
deployments.

<h3 class="pdoc-module-header" id="Key" data-link-title="Key">
    <a href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/ssl/key.ts#L25">
        Resource <strong>Key</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>class</span> <span class='nx'>Key</span> <span class='kr'>extends</span> <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResource'>CustomResource</a></code></pre>

`f5bigip.ssl.Key` This resource will import SSL certificate key on BIG-IP LTM.
Certificate key can be imported from certificate key files on the local disk, in PEM format

#### Example Usage

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as f5bigip from "@pulumi/f5bigip";
import * from "fs";

const test_key = new f5bigip.ssl.Key("test-key", {
    name: "serverkey.key",
    content: fs.readFileSync("serverkey.key"),
    partition: "Common",
});
```

<h4 class="pdoc-member-header" id="Key-constructor">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/ssl/key.ts#L64"> <b>constructor</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span><span class='kd'>new</span> Key(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, args: <a href='#KeyArgs'>KeyArgs</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>)</code></pre>


Create a Key resource with the given unique name, arguments, and options.

* `name` The _unique_ name of the resource.
* `args` The arguments to use to populate this resource&#39;s properties.
* `opts` A bag of options that control this resource&#39;s behavior.

<h4 class="pdoc-member-header" id="Key-get">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/ssl/key.ts#L35">method <b>get</b></a>
</h4>


<pre class="highlight"><code><span class='kd'>public static </span>get(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>pulumi.ID</a>&gt;, state?: <a href='#KeyState'>KeyState</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>): <a href='#Key'>Key</a></code></pre>


Get an existing Key resource's state with the given name, ID, and optional extra
properties used to qualify the lookup.

<h4 class="pdoc-member-header" id="Key-getProvider">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/ssl/key.ts#L25">method <b>getProvider</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>getProvider(moduleMember: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>): <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ProviderResource'>ProviderResource</a> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span></code></pre>

<h4 class="pdoc-member-header" id="Key-isInstance">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/ssl/key.ts#L46">method <b>isInstance</b></a>
</h4>


<pre class="highlight"><code><span class='kd'>public static </span>isInstance(obj: <span class='kd'><a href='https://www.typescriptlang.org/docs/handbook/basic-types.html#any'>any</a></span>): obj is Key</code></pre>


Returns true if the given object is an instance of Key.  This is designed to work even
when multiple copies of the Pulumi SDK have been loaded into the same process.

<h4 class="pdoc-member-header" id="Key-content">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/ssl/key.ts#L56">property <b>content</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>content: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Content of SSL certificate key present on local Disk

<h4 class="pdoc-member-header" id="Key-id">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/ssl/key.ts#L25">property <b>id</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>ID</a>&gt;;</code></pre>

id is the provider-assigned unique ID for this managed resource.  It is set during
deployments and may be missing (undefined) during planning phases.

<h4 class="pdoc-member-header" id="Key-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/ssl/key.ts#L60">property <b>name</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>name: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Name of the SSL Certificate key to be Imported on to BIGIP

<h4 class="pdoc-member-header" id="Key-partition">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/ssl/key.ts#L64">property <b>partition</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>partition: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span>&gt;;</code></pre>

Partition on to SSL Certificate key to be imported

<h4 class="pdoc-member-header" id="Key-urn">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/ssl/key.ts#L25">property <b>urn</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>urn: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#URN'>URN</a>&gt;;</code></pre>

urn is the stable logical URN used to distinctly address a resource, both before and after
deployments.


<h2 id="functions">Functions</h2>
<h3 class="pdoc-module-header" id="getCertificate" data-link-title="getCertificate">
    <a href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/ssl/getCertificate.ts#L8">
        Function <strong>getCertificate</strong>
    </a>
</h3>


<pre class="highlight"><code><span class='kd'></span>getCertificate(args: <a href='#GetCertificateArgs'>GetCertificateArgs</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions'>pulumi.InvokeOptions</a>): <a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise'>Promise</a>&lt;<a href='#GetCertificateResult'>GetCertificateResult</a>&gt;</code></pre>


<h2 id="apis">Others</h2>
<h3 class="pdoc-module-header" id="CertificateArgs" data-link-title="CertificateArgs">
    <a href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/ssl/certificate.ts#L125">
        interface <strong>CertificateArgs</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>CertificateArgs</span></code></pre>

The set of arguments for constructing a Certificate resource.

<h4 class="pdoc-member-header" id="CertificateArgs-content">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/ssl/certificate.ts#L129">property <b>content</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>content: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Content of certificate on Disk

<h4 class="pdoc-member-header" id="CertificateArgs-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/ssl/certificate.ts#L133">property <b>name</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>name: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Name of the SSL Certificate to be Imported on to BIGIP

<h4 class="pdoc-member-header" id="CertificateArgs-partition">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/ssl/certificate.ts#L137">property <b>partition</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>partition?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Partition on to SSL Certificate to be imported

<h3 class="pdoc-module-header" id="CertificateState" data-link-title="CertificateState">
    <a href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/ssl/certificate.ts#L107">
        interface <strong>CertificateState</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>CertificateState</span></code></pre>

Input properties used for looking up and filtering Certificate resources.

<h4 class="pdoc-member-header" id="CertificateState-content">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/ssl/certificate.ts#L111">property <b>content</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>content?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Content of certificate on Disk

<h4 class="pdoc-member-header" id="CertificateState-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/ssl/certificate.ts#L115">property <b>name</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>name?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Name of the SSL Certificate to be Imported on to BIGIP

<h4 class="pdoc-member-header" id="CertificateState-partition">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/ssl/certificate.ts#L119">property <b>partition</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>partition?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Partition on to SSL Certificate to be imported

<h3 class="pdoc-module-header" id="GetCertificateArgs" data-link-title="GetCertificateArgs">
    <a href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/ssl/getCertificate.ts#L25">
        interface <strong>GetCertificateArgs</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>GetCertificateArgs</span></code></pre>

A collection of arguments for invoking getCertificate.

<h4 class="pdoc-member-header" id="GetCertificateArgs-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/ssl/getCertificate.ts#L26">property <b>name</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>
<h4 class="pdoc-member-header" id="GetCertificateArgs-partition">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/ssl/getCertificate.ts#L27">property <b>partition</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>partition: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>
<h3 class="pdoc-module-header" id="GetCertificateResult" data-link-title="GetCertificateResult">
    <a href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/ssl/getCertificate.ts#L33">
        interface <strong>GetCertificateResult</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>GetCertificateResult</span></code></pre>

A collection of values returned by getCertificate.

<h4 class="pdoc-member-header" id="GetCertificateResult-certificate">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/ssl/getCertificate.ts#L34">property <b>certificate</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>certificate: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>
<h4 class="pdoc-member-header" id="GetCertificateResult-id">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/ssl/getCertificate.ts#L38">property <b>id</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>id: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>

The provider-assigned unique ID for this managed resource.

<h4 class="pdoc-member-header" id="GetCertificateResult-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/ssl/getCertificate.ts#L39">property <b>name</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>
<h4 class="pdoc-member-header" id="GetCertificateResult-partition">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/ssl/getCertificate.ts#L40">property <b>partition</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>partition: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>
<h3 class="pdoc-module-header" id="KeyArgs" data-link-title="KeyArgs">
    <a href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/ssl/key.ts#L125">
        interface <strong>KeyArgs</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>KeyArgs</span></code></pre>

The set of arguments for constructing a Key resource.

<h4 class="pdoc-member-header" id="KeyArgs-content">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/ssl/key.ts#L129">property <b>content</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>content: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Content of SSL certificate key present on local Disk

<h4 class="pdoc-member-header" id="KeyArgs-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/ssl/key.ts#L133">property <b>name</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>name: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Name of the SSL Certificate key to be Imported on to BIGIP

<h4 class="pdoc-member-header" id="KeyArgs-partition">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/ssl/key.ts#L137">property <b>partition</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>partition?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Partition on to SSL Certificate key to be imported

<h3 class="pdoc-module-header" id="KeyState" data-link-title="KeyState">
    <a href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/ssl/key.ts#L107">
        interface <strong>KeyState</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>KeyState</span></code></pre>

Input properties used for looking up and filtering Key resources.

<h4 class="pdoc-member-header" id="KeyState-content">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/ssl/key.ts#L111">property <b>content</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>content?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Content of SSL certificate key present on local Disk

<h4 class="pdoc-member-header" id="KeyState-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/ssl/key.ts#L115">property <b>name</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>name?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Name of the SSL Certificate key to be Imported on to BIGIP

<h4 class="pdoc-member-header" id="KeyState-partition">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/ssl/key.ts#L119">property <b>partition</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>partition?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Partition on to SSL Certificate key to be imported

