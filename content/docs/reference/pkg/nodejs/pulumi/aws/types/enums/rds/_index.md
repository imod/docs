---
title: "Module types/enums/rds"
title_tag: "Module types/enums/rds | Package @pulumi/aws | Node.js SDK"
linktitle: "enums/rds"
meta_desc: "Explore members of the enums/rds module in the @pulumi/aws package."
git_sha: "6c9e985f93682e9b4056b497c1a31a75fd7884fc"
block_external_search_index: true
---

<!-- WARNING: this page was generated by a tool. Do not edit it by hand. -->
<!-- To change it, please see https://github.com/pulumi/docs/tree/master/tools/tscdocgen. -->

{{< resource-docs-alert "aws" >}}






<h3>APIs</h3>
<ul class="api">
    <li><a href="#EngineMode"><span class="symbol api"></span>EngineMode</a></li>
    <li><a href="#EngineType"><span class="symbol api"></span>EngineType</a></li>
    <li><a href="#InstanceType"><span class="symbol api"></span>InstanceType</a></li>
    <li><a href="#StorageType"><span class="symbol api"></span>StorageType</a></li>
</ul>




<h2 id="apis">APIs</h2>
<h3 class="pdoc-module-header" id="EngineMode" data-link-title="EngineMode">
    <a href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/types/enums/rds/index.ts#L12">
        type <strong>EngineMode</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kd'>type</span> EngineMode = <span class='s2'>"provisioned"</span> | <span class='s2'>"serverless"</span> | <span class='s2'>"parallelquery"</span> | <span class='s2'>"global"</span>;</code></pre>
<h3 class="pdoc-module-header" id="EngineType" data-link-title="EngineType">
    <a href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/types/enums/rds/index.ts#L20">
        type <strong>EngineType</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kd'>type</span> EngineType = <span class='s2'>"aurora"</span> | <span class='s2'>"aurora-mysql"</span> | <span class='s2'>"aurora-postgresql"</span>;</code></pre>
<h3 class="pdoc-module-header" id="InstanceType" data-link-title="InstanceType">
    <a href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/types/enums/rds/index.ts#L84">
        type <strong>InstanceType</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kd'>type</span> InstanceType = <span class='s2'>"db.t3.micro"</span> | <span class='s2'>"db.t3.small"</span> | <span class='s2'>"db.t3.medium"</span> | <span class='s2'>"db.t3.large"</span> | <span class='s2'>"db.t3.xlarge"</span> | <span class='s2'>"db.t3.2xlarge"</span> | <span class='s2'>"db.t2.micro"</span> | <span class='s2'>"db.t2.small"</span> | <span class='s2'>"db.t2.medium"</span> | <span class='s2'>"db.t2.large"</span> | <span class='s2'>"db.t2.xlarge"</span> | <span class='s2'>"db.t2.2xlarge"</span> | <span class='s2'>"db.m1.small"</span> | <span class='s2'>"db.m1.medium"</span> | <span class='s2'>"db.m1.large"</span> | <span class='s2'>"db.m1.xlarge"</span> | <span class='s2'>"db.m2.xlarge"</span> | <span class='s2'>"db.m2.2xlarge"</span> | <span class='s2'>"db.m2.4xlarge"</span> | <span class='s2'>"db.m3.medium"</span> | <span class='s2'>"db.m3.large"</span> | <span class='s2'>"db.m3.xlarge"</span> | <span class='s2'>"db.m3.2xlarge"</span> | <span class='s2'>"db.m4.large"</span> | <span class='s2'>"db.m4.xlarge"</span> | <span class='s2'>"db.m4.2xlarge"</span> | <span class='s2'>"db.m4.4xlarge"</span> | <span class='s2'>"db.m4.10xlarge"</span> | <span class='s2'>"db.m5.large"</span> | <span class='s2'>"db.m5.xlarge"</span> | <span class='s2'>"db.m5.2xlarge"</span> | <span class='s2'>"db.m5.4xlarge"</span> | <span class='s2'>"db.m5.12xlarge"</span> | <span class='s2'>"db.m5.24xlarge"</span> | <span class='s2'>"db.r3.large"</span> | <span class='s2'>"db.r3.xlarge"</span> | <span class='s2'>"db.r3.2xlarge"</span> | <span class='s2'>"db.r3.4xlarge"</span> | <span class='s2'>"db.r3.8xlarge"</span> | <span class='s2'>"db.r4.large"</span> | <span class='s2'>"db.r4.xlarge"</span> | <span class='s2'>"db.r4.2xlarge"</span> | <span class='s2'>"db.r4.4xlarge"</span> | <span class='s2'>"db.r4.8xlarge"</span> | <span class='s2'>"db.r4.16xlarge"</span> | <span class='s2'>"db.r5.large"</span> | <span class='s2'>"db.r5.xlarge"</span> | <span class='s2'>"db.r5.2xlarge"</span> | <span class='s2'>"db.r5.4xlarge"</span> | <span class='s2'>"db.r5.12xlarge"</span> | <span class='s2'>"db.r5.24xlarge"</span> | <span class='s2'>"db.x1.16xlarge"</span> | <span class='s2'>"db.x1.32xlarge"</span> | <span class='s2'>"db.x1e.xlarge"</span> | <span class='s2'>"db.x1e.2xlarge"</span> | <span class='s2'>"db.x1e.4xlarge"</span> | <span class='s2'>"db.x1e.8xlarge"</span> | <span class='s2'>"db.x1e.32xlarge"</span>;</code></pre>
<h3 class="pdoc-module-header" id="StorageType" data-link-title="StorageType">
    <a href="https://github.com/pulumi/pulumi-aws/blob/6c9e985f93682e9b4056b497c1a31a75fd7884fc/sdk/nodejs/types/enums/rds/index.ts#L92">
        type <strong>StorageType</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kd'>type</span> StorageType = <span class='s2'>"standard"</span> | <span class='s2'>"gp2"</span> | <span class='s2'>"io1"</span>;</code></pre>
