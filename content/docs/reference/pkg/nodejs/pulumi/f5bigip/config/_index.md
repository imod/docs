---
title: "Module config"
title_tag: "Module config | Package @pulumi/f5bigip | Node.js SDK"
linktitle: "config"
meta_desc: "Explore members of the config module in the @pulumi/f5bigip package."
git_sha: "4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14"
block_external_search_index: true
---

<!-- WARNING: this page was generated by a tool. Do not edit it by hand. -->
<!-- To change it, please see https://github.com/pulumi/docs/tree/master/tools/tscdocgen. -->

{{< resource-docs-alert "f5bigip" >}}






<h3>APIs</h3>
<ul class="api">
    <li><a href="#address"><span class="symbol api"></span>address</a></li>
    <li><a href="#loginRef"><span class="symbol api"></span>loginRef</a></li>
    <li><a href="#password"><span class="symbol api"></span>password</a></li>
    <li><a href="#port"><span class="symbol api"></span>port</a></li>
    <li><a href="#teemDisable"><span class="symbol api"></span>teemDisable</a></li>
    <li><a href="#tokenAuth"><span class="symbol api"></span>tokenAuth</a></li>
    <li><a href="#username"><span class="symbol api"></span>username</a></li>
</ul>




<h2 id="apis">APIs</h2>
<h3 class="pdoc-module-header" id="address" data-link-title="address">
    <a href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/config/vars.ts#L12">
        let <strong>address</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kd'>let</span> address: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span> = <span class='s2'> __config.get(&#34;address&#34;)</span>;</code></pre>

Domain name/IP of the BigIP

<h3 class="pdoc-module-header" id="loginRef" data-link-title="loginRef">
    <a href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/config/vars.ts#L16">
        let <strong>loginRef</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kd'>let</span> loginRef: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span> = <span class='s2'> __config.get(&#34;loginRef&#34;)</span>;</code></pre>

Login reference for token authentication (see BIG-IP REST docs for details)

<h3 class="pdoc-module-header" id="password" data-link-title="password">
    <a href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/config/vars.ts#L20">
        let <strong>password</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kd'>let</span> password: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span> = <span class='s2'> __config.get(&#34;password&#34;)</span>;</code></pre>

The user's password

<h3 class="pdoc-module-header" id="port" data-link-title="port">
    <a href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/config/vars.ts#L24">
        let <strong>port</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kd'>let</span> port: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span> = <span class='s2'> __config.get(&#34;port&#34;)</span>;</code></pre>

Management Port to connect to Bigip

<h3 class="pdoc-module-header" id="teemDisable" data-link-title="teemDisable">
    <a href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/config/vars.ts#L28">
        let <strong>teemDisable</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kd'>let</span> teemDisable: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean'>boolean</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span> = <span class='s2'> __config.getObject&lt;boolean&gt;(&#34;teemDisable&#34;)</span>;</code></pre>

If this flag set to true,sending telemetry data to TEEM will be disabled

<h3 class="pdoc-module-header" id="tokenAuth" data-link-title="tokenAuth">
    <a href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/config/vars.ts#L32">
        let <strong>tokenAuth</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kd'>let</span> tokenAuth: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean'>boolean</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span> = <span class='s2'> __config.getObject&lt;boolean&gt;(&#34;tokenAuth&#34;)</span>;</code></pre>

Enable to use an external authentication source (LDAP, TACACS, etc)

<h3 class="pdoc-module-header" id="username" data-link-title="username">
    <a href="https://github.com/pulumi/pulumi-f5bigip/blob/4021ae00c4660c7f8fb943bfa9ecd3fe1fad3a14/sdk/nodejs/config/vars.ts#L36">
        let <strong>username</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kd'>let</span> username: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span> = <span class='s2'> __config.get(&#34;username&#34;)</span>;</code></pre>

Username with API access to the BigIP

