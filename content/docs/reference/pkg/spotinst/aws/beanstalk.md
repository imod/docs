
---
title: "Beanstalk"
block_external_search_index: true
---



Provides a Spotinst AWS group resource using Elastic Beanstalk.

## Example Usage

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as spotinst from "@pulumi/spotinst";

const elastigoup_aws_beanstalk = new spotinst.aws.Beanstalk("elastigoup-aws-beanstalk", {
    beanstalkEnvironmentId: "e-example",
    beanstalkEnvironmentName: "example-env",
    deploymentPreferences: {
        automaticRoll: true,
        batchSizePercentage: 100,
        gracePeriod: 90,
        strategies: [{
            action: "REPLACE_SERVER",
            shouldDrainInstances: true,
        }],
    },
    desiredCapacity: 0,
    instanceTypesSpots: [
        "t2.micro",
        "t2.medium",
        "t2.large",
    ],
    managedActions: {
        platformUpdate: {
            performAt: "timeWindow",
            timeWindow: "Mon:23:50-Tue:00:20",
            updateLevel: "minorAndPatch",
        },
    },
    maxSize: 1,
    minSize: 0,
    product: "Linux/UNIX",
    region: "us-west-2",
});
```

## Scheduled Tasks

Each `scheduled_task` supports the following:

* `task_type` - (Required) The task type to run. Supported task types are: `"scale"`, `"backup_ami"`, `"roll"`, `"scaleUp"`, `"percentageScaleUp"`, `"scaleDown"`, `"percentageScaleDown"`, `"statefulUpdateCapacity"`.
* `cron_expression` - (Optional; Required if not using `frequency`) A valid cron expression. The cron is running in UTC time zone and is in [Unix cron format](https://en.wikipedia.org/wiki/Cron).
* `start_time` - (Optional; Format: ISO 8601) Set a start time for one time tasks.
* `frequency` - (Optional; Required if not using `cron_expression`) The recurrence frequency to run this task. Supported values are `"hourly"`, `"daily"`, `"weekly"` and `"continuous"`.
* `scale_target_capacity` - (Optional) The desired number of instances the group should have.
* `scale_min_capacity` - (Optional) The minimum number of instances the group should have.
* `scale_max_capacity` - (Optional) The maximum number of instances the group should have.
* `is_enabled` - (Optional, Default: `true`) Setting the task to being enabled or disabled.
* `target_capacity` - (Optional; Only valid for statefulUpdateCapacity) The desired number of instances the group should have.
* `min_capacity` - (Optional; Only valid for statefulUpdateCapacity) The minimum number of instances the group should have.
* `max_capacity` - (Optional; Only valid for statefulUpdateCapacity) The maximum number of instances the group should have.
* `batch_size_percentage` - (Optional; Required when the `task_type` is `"roll"`.) The percentage size of each batch in the scheduled deployment roll.
* `grace_period` - (Optional) The period of time (seconds) to wait before checking a batch's health after it's deployment.
* `adjustment` - (Optional; Min 1) The number of instances to add or remove.
* `adjustment_percentage` - (Optional; Min 1) The percentage of instances to add or remove.

Usage:

```typescript
import * as pulumi from "@pulumi/pulumi";
```

> This content is derived from https://github.com/terraform-providers/terraform-provider-spotinst/blob/master/website/docs/r/elastigroup_aws_beanstalk.html.markdown.



## Create a Beanstalk Resource

{{< chooser language "javascript,typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/spotinst/aws/#Beanstalk">Beanstalk</a></span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">args</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/spotinst/aws/#BeanstalkArgs">BeanstalkArgs</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">pulumi.CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span><span class="nf">Beanstalk</span><span class="p">(resource_name, opts=None, </span>beanstalk_environment_id=None<span class="p">, </span>beanstalk_environment_name=None<span class="p">, </span>deployment_preferences=None<span class="p">, </span>desired_capacity=None<span class="p">, </span>instance_types_spots=None<span class="p">, </span>maintenance=None<span class="p">, </span>managed_actions=None<span class="p">, </span>max_size=None<span class="p">, </span>min_size=None<span class="p">, </span>name=None<span class="p">, </span>product=None<span class="p">, </span>region=None<span class="p">, </span>scheduled_tasks=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>NewBeanstalk<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">pulumi.Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">args</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-spotinst/sdk/go/spotinst/aws?tab=doc#BeanstalkArgs">BeanstalkArgs</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">pulumi.ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-spotinst/sdk/go/spotinst/aws?tab=doc#Beanstalk">Beanstalk</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Spotinst/Pulumi.Spotinst.Aws.Beanstalk.html">Beanstalk</a></span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Spotinst/Pulumi.Spotinst.Aws.BeanstalkArgs.html">BeanstalkArgs</a></span> <span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language nodejs %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resource.</dd>
    <dt class="property-optional" title="Optional">
        <span>args</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The arguments to use to populate this resource's properties.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resource.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>
{{% /choosable %}}

{{% choosable language go %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resource.</dd>
    <dt class="property-optional" title="Optional">
        <span>args</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The arguments to use to populate this resource's properties.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

{{% choosable language csharp %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resource.</dd>
    <dt class="property-optional" title="Optional">
        <span>args</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The arguments to use to populate this resource's properties.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

#### Resource Arguments




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Beanstalk<wbr>Environment<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The id of an existing Beanstalk environment. 
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Beanstalk<wbr>Environment<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of an existing Beanstalk environment.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Deployment<wbr>Preferences</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#beanstalkdeploymentpreferences">Beanstalk<wbr>Deployment<wbr>Preferences<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Preferences when performing a roll
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Desired<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The desired number of instances the group should have at any time.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Instance<wbr>Types<wbr>Spots</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string></span>
    </dt>
    <dd>{{% md %}}One or more instance types. To maximize the availability of Spot instances, select as many instance types as possible.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Maintenance</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Managed<wbr>Actions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#beanstalkmanagedactions">Beanstalk<wbr>Managed<wbr>Actions<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Managed Actions parameters
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Max<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The maximum number of instances the group should have at any time.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Min<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The minimum number of instances the group should have at any time.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The group name.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Product</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Operation system type. Valid values: `"Linux/UNIX"`, `"SUSE Linux"`, `"Windows"`.
For EC2 Classic instances:  `"Linux/UNIX (Amazon VPC)"`, `"SUSE Linux (Amazon VPC)"`, `"Windows (Amazon VPC)"`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Region</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The AWS region your group will be created in. Cannot be changed after the group has been created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Scheduled<wbr>Tasks</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#beanstalkscheduledtask">List&lt;Beanstalk<wbr>Scheduled<wbr>Task<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Beanstalk<wbr>Environment<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The id of an existing Beanstalk environment. 
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Beanstalk<wbr>Environment<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The name of an existing Beanstalk environment.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Deployment<wbr>Preferences</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#beanstalkdeploymentpreferences">*Beanstalk<wbr>Deployment<wbr>Preferences</a></span>
    </dt>
    <dd>{{% md %}}Preferences when performing a roll
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Desired<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The desired number of instances the group should have at any time.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Instance<wbr>Types<wbr>Spots</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}One or more instance types. To maximize the availability of Spot instances, select as many instance types as possible.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Maintenance</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Managed<wbr>Actions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#beanstalkmanagedactions">*Beanstalk<wbr>Managed<wbr>Actions</a></span>
    </dt>
    <dd>{{% md %}}Managed Actions parameters
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Max<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The maximum number of instances the group should have at any time.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Min<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The minimum number of instances the group should have at any time.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The group name.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Product</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Operation system type. Valid values: `"Linux/UNIX"`, `"SUSE Linux"`, `"Windows"`.
For EC2 Classic instances:  `"Linux/UNIX (Amazon VPC)"`, `"SUSE Linux (Amazon VPC)"`, `"Windows (Amazon VPC)"`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Region</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The AWS region your group will be created in. Cannot be changed after the group has been created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Scheduled<wbr>Tasks</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#beanstalkscheduledtask">[]Beanstalk<wbr>Scheduled<wbr>Task</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>beanstalk<wbr>Environment<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The id of an existing Beanstalk environment. 
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>beanstalk<wbr>Environment<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of an existing Beanstalk environment.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>deployment<wbr>Preferences</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#beanstalkdeploymentpreferences">Beanstalk<wbr>Deployment<wbr>Preferences?</a></span>
    </dt>
    <dd>{{% md %}}Preferences when performing a roll
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>desired<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The desired number of instances the group should have at any time.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>instance<wbr>Types<wbr>Spots</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}One or more instance types. To maximize the availability of Spot instances, select as many instance types as possible.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>maintenance</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>managed<wbr>Actions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#beanstalkmanagedactions">Beanstalk<wbr>Managed<wbr>Actions?</a></span>
    </dt>
    <dd>{{% md %}}Managed Actions parameters
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>max<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The maximum number of instances the group should have at any time.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>min<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The minimum number of instances the group should have at any time.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The group name.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>product</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Operation system type. Valid values: `"Linux/UNIX"`, `"SUSE Linux"`, `"Windows"`.
For EC2 Classic instances:  `"Linux/UNIX (Amazon VPC)"`, `"SUSE Linux (Amazon VPC)"`, `"Windows (Amazon VPC)"`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>region</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The AWS region your group will be created in. Cannot be changed after the group has been created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>scheduled<wbr>Tasks</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#beanstalkscheduledtask">Beanstalk<wbr>Scheduled<wbr>Task[]?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>beanstalk_<wbr>environment_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The id of an existing Beanstalk environment. 
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>beanstalk_<wbr>environment_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of an existing Beanstalk environment.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>deployment_<wbr>preferences</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#beanstalkdeploymentpreferences">Dict[Beanstalk<wbr>Deployment<wbr>Preferences]</a></span>
    </dt>
    <dd>{{% md %}}Preferences when performing a roll
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>desired_<wbr>capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The desired number of instances the group should have at any time.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>instance_<wbr>types_<wbr>spots</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}One or more instance types. To maximize the availability of Spot instances, select as many instance types as possible.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>maintenance</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>managed_<wbr>actions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#beanstalkmanagedactions">Dict[Beanstalk<wbr>Managed<wbr>Actions]</a></span>
    </dt>
    <dd>{{% md %}}Managed Actions parameters
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>max_<wbr>size</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The maximum number of instances the group should have at any time.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>min_<wbr>size</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The minimum number of instances the group should have at any time.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The group name.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>product</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Operation system type. Valid values: `"Linux/UNIX"`, `"SUSE Linux"`, `"Windows"`.
For EC2 Classic instances:  `"Linux/UNIX (Amazon VPC)"`, `"SUSE Linux (Amazon VPC)"`, `"Windows (Amazon VPC)"`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>region</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The AWS region your group will be created in. Cannot be changed after the group has been created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>scheduled_<wbr>tasks</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#beanstalkscheduledtask">List[Beanstalk<wbr>Scheduled<wbr>Task]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}







## Beanstalk Output Properties

The following output properties are available:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Beanstalk<wbr>Environment<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The id of an existing Beanstalk environment. 
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Beanstalk<wbr>Environment<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of an existing Beanstalk environment.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Deployment<wbr>Preferences</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#beanstalkdeploymentpreferences">Beanstalk<wbr>Deployment<wbr>Preferences?</a></span>
    </dt>
    <dd>{{% md %}}Preferences when performing a roll
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Desired<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The desired number of instances the group should have at any time.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Instance<wbr>Types<wbr>Spots</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string></span>
    </dt>
    <dd>{{% md %}}One or more instance types. To maximize the availability of Spot instances, select as many instance types as possible.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Maintenance</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Managed<wbr>Actions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#beanstalkmanagedactions">Beanstalk<wbr>Managed<wbr>Actions?</a></span>
    </dt>
    <dd>{{% md %}}Managed Actions parameters
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Max<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The maximum number of instances the group should have at any time.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Min<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The minimum number of instances the group should have at any time.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The group name.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Product</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Operation system type. Valid values: `"Linux/UNIX"`, `"SUSE Linux"`, `"Windows"`.
For EC2 Classic instances:  `"Linux/UNIX (Amazon VPC)"`, `"SUSE Linux (Amazon VPC)"`, `"Windows (Amazon VPC)"`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Region</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The AWS region your group will be created in. Cannot be changed after the group has been created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Scheduled<wbr>Tasks</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#beanstalkscheduledtask">List&lt;Beanstalk<wbr>Scheduled<wbr>Task&gt;?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Beanstalk<wbr>Environment<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The id of an existing Beanstalk environment. 
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Beanstalk<wbr>Environment<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The name of an existing Beanstalk environment.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Deployment<wbr>Preferences</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#beanstalkdeploymentpreferences">*Beanstalk<wbr>Deployment<wbr>Preferences</a></span>
    </dt>
    <dd>{{% md %}}Preferences when performing a roll
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Desired<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The desired number of instances the group should have at any time.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Instance<wbr>Types<wbr>Spots</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}One or more instance types. To maximize the availability of Spot instances, select as many instance types as possible.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Maintenance</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Managed<wbr>Actions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#beanstalkmanagedactions">*Beanstalk<wbr>Managed<wbr>Actions</a></span>
    </dt>
    <dd>{{% md %}}Managed Actions parameters
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Max<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The maximum number of instances the group should have at any time.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Min<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The minimum number of instances the group should have at any time.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The group name.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Product</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Operation system type. Valid values: `"Linux/UNIX"`, `"SUSE Linux"`, `"Windows"`.
For EC2 Classic instances:  `"Linux/UNIX (Amazon VPC)"`, `"SUSE Linux (Amazon VPC)"`, `"Windows (Amazon VPC)"`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Region</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The AWS region your group will be created in. Cannot be changed after the group has been created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Scheduled<wbr>Tasks</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#beanstalkscheduledtask">[]Beanstalk<wbr>Scheduled<wbr>Task</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>beanstalk<wbr>Environment<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The id of an existing Beanstalk environment. 
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>beanstalk<wbr>Environment<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of an existing Beanstalk environment.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>deployment<wbr>Preferences</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#beanstalkdeploymentpreferences">Beanstalk<wbr>Deployment<wbr>Preferences?</a></span>
    </dt>
    <dd>{{% md %}}Preferences when performing a roll
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>desired<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The desired number of instances the group should have at any time.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>instance<wbr>Types<wbr>Spots</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}One or more instance types. To maximize the availability of Spot instances, select as many instance types as possible.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>maintenance</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>managed<wbr>Actions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#beanstalkmanagedactions">Beanstalk<wbr>Managed<wbr>Actions?</a></span>
    </dt>
    <dd>{{% md %}}Managed Actions parameters
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>max<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The maximum number of instances the group should have at any time.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>min<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The minimum number of instances the group should have at any time.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The group name.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>product</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Operation system type. Valid values: `"Linux/UNIX"`, `"SUSE Linux"`, `"Windows"`.
For EC2 Classic instances:  `"Linux/UNIX (Amazon VPC)"`, `"SUSE Linux (Amazon VPC)"`, `"Windows (Amazon VPC)"`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>region</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The AWS region your group will be created in. Cannot be changed after the group has been created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>scheduled<wbr>Tasks</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#beanstalkscheduledtask">Beanstalk<wbr>Scheduled<wbr>Task[]?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>beanstalk_<wbr>environment_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The id of an existing Beanstalk environment. 
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>beanstalk_<wbr>environment_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of an existing Beanstalk environment.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>deployment_<wbr>preferences</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#beanstalkdeploymentpreferences">Dict[Beanstalk<wbr>Deployment<wbr>Preferences]</a></span>
    </dt>
    <dd>{{% md %}}Preferences when performing a roll
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>desired_<wbr>capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The desired number of instances the group should have at any time.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>instance_<wbr>types_<wbr>spots</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}One or more instance types. To maximize the availability of Spot instances, select as many instance types as possible.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>maintenance</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>managed_<wbr>actions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#beanstalkmanagedactions">Dict[Beanstalk<wbr>Managed<wbr>Actions]</a></span>
    </dt>
    <dd>{{% md %}}Managed Actions parameters
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>max_<wbr>size</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The maximum number of instances the group should have at any time.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>min_<wbr>size</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The minimum number of instances the group should have at any time.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The group name.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>product</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Operation system type. Valid values: `"Linux/UNIX"`, `"SUSE Linux"`, `"Windows"`.
For EC2 Classic instances:  `"Linux/UNIX (Amazon VPC)"`, `"SUSE Linux (Amazon VPC)"`, `"Windows (Amazon VPC)"`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>region</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The AWS region your group will be created in. Cannot be changed after the group has been created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>scheduled_<wbr>tasks</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#beanstalkscheduledtask">List[Beanstalk<wbr>Scheduled<wbr>Task]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## Look up an Existing Beanstalk Resource

Get an existing Beanstalk resource's state with the given name, ID, and optional extra properties used to qualify the lookup.

{{< chooser language "javascript,typescript,python,go,csharp  " / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">id</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">, </span><span class="nx">state</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/spotinst/aws/#BeanstalkState">BeanstalkState</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/spotinst/aws/#Beanstalk">Beanstalk</a></span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">static </span><span class="nf">get</span><span class="p">(resource_name, id, opts=None, </span>beanstalk_environment_id=None<span class="p">, </span>beanstalk_environment_name=None<span class="p">, </span>deployment_preferences=None<span class="p">, </span>desired_capacity=None<span class="p">, </span>instance_types_spots=None<span class="p">, </span>maintenance=None<span class="p">, </span>managed_actions=None<span class="p">, </span>max_size=None<span class="p">, </span>min_size=None<span class="p">, </span>name=None<span class="p">, </span>product=None<span class="p">, </span>region=None<span class="p">, </span>scheduled_tasks=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetBeanstalk<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">id</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">, </span><span class="nx">state</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-spotinst/sdk/go/spotinst/aws?tab=doc#BeanstalkState">BeanstalkState</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-spotinst/sdk/go/spotinst/aws?tab=doc#Beanstalk">Beanstalk</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Spotinst/Pulumi.Spotinst.Aws.Beanstalk.html">Beanstalk</a></span><span class="nf"> Get</span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input.html">Input&lt;string&gt;</a></span> <span class="nx">id<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Spotinst/Pulumi.Spotinst.Aws.BeanstalkState.html">BeanstalkState</a></span>? <span class="nx">state<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language nodejs %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>state</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>Any extra arguments used during the lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>resource_name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Optional">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
</dl>
{{% /choosable %}}

{{% choosable language go %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>state</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>Any extra arguments used during the lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

{{% choosable language csharp %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>state</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>Any extra arguments used during the lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

The following state arguments are supported:



{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Beanstalk<wbr>Environment<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The id of an existing Beanstalk environment. 
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Beanstalk<wbr>Environment<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of an existing Beanstalk environment.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Deployment<wbr>Preferences</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#beanstalkdeploymentpreferences">Beanstalk<wbr>Deployment<wbr>Preferences<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Preferences when performing a roll
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Desired<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The desired number of instances the group should have at any time.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Instance<wbr>Types<wbr>Spots</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}One or more instance types. To maximize the availability of Spot instances, select as many instance types as possible.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Maintenance</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Managed<wbr>Actions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#beanstalkmanagedactions">Beanstalk<wbr>Managed<wbr>Actions<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Managed Actions parameters
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The maximum number of instances the group should have at any time.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Min<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The minimum number of instances the group should have at any time.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The group name.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Product</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Operation system type. Valid values: `"Linux/UNIX"`, `"SUSE Linux"`, `"Windows"`.
For EC2 Classic instances:  `"Linux/UNIX (Amazon VPC)"`, `"SUSE Linux (Amazon VPC)"`, `"Windows (Amazon VPC)"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Region</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The AWS region your group will be created in. Cannot be changed after the group has been created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Scheduled<wbr>Tasks</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#beanstalkscheduledtask">List&lt;Beanstalk<wbr>Scheduled<wbr>Task<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Beanstalk<wbr>Environment<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The id of an existing Beanstalk environment. 
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Beanstalk<wbr>Environment<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The name of an existing Beanstalk environment.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Deployment<wbr>Preferences</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#beanstalkdeploymentpreferences">*Beanstalk<wbr>Deployment<wbr>Preferences</a></span>
    </dt>
    <dd>{{% md %}}Preferences when performing a roll
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Desired<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The desired number of instances the group should have at any time.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Instance<wbr>Types<wbr>Spots</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}One or more instance types. To maximize the availability of Spot instances, select as many instance types as possible.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Maintenance</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Managed<wbr>Actions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#beanstalkmanagedactions">*Beanstalk<wbr>Managed<wbr>Actions</a></span>
    </dt>
    <dd>{{% md %}}Managed Actions parameters
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The maximum number of instances the group should have at any time.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Min<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The minimum number of instances the group should have at any time.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The group name.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Product</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Operation system type. Valid values: `"Linux/UNIX"`, `"SUSE Linux"`, `"Windows"`.
For EC2 Classic instances:  `"Linux/UNIX (Amazon VPC)"`, `"SUSE Linux (Amazon VPC)"`, `"Windows (Amazon VPC)"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Region</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The AWS region your group will be created in. Cannot be changed after the group has been created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Scheduled<wbr>Tasks</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#beanstalkscheduledtask">[]Beanstalk<wbr>Scheduled<wbr>Task</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>beanstalk<wbr>Environment<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The id of an existing Beanstalk environment. 
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>beanstalk<wbr>Environment<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of an existing Beanstalk environment.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>deployment<wbr>Preferences</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#beanstalkdeploymentpreferences">Beanstalk<wbr>Deployment<wbr>Preferences?</a></span>
    </dt>
    <dd>{{% md %}}Preferences when performing a roll
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>desired<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The desired number of instances the group should have at any time.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>instance<wbr>Types<wbr>Spots</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}One or more instance types. To maximize the availability of Spot instances, select as many instance types as possible.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>maintenance</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>managed<wbr>Actions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#beanstalkmanagedactions">Beanstalk<wbr>Managed<wbr>Actions?</a></span>
    </dt>
    <dd>{{% md %}}Managed Actions parameters
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The maximum number of instances the group should have at any time.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>min<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The minimum number of instances the group should have at any time.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The group name.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>product</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Operation system type. Valid values: `"Linux/UNIX"`, `"SUSE Linux"`, `"Windows"`.
For EC2 Classic instances:  `"Linux/UNIX (Amazon VPC)"`, `"SUSE Linux (Amazon VPC)"`, `"Windows (Amazon VPC)"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>region</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The AWS region your group will be created in. Cannot be changed after the group has been created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>scheduled<wbr>Tasks</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#beanstalkscheduledtask">Beanstalk<wbr>Scheduled<wbr>Task[]?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>beanstalk_<wbr>environment_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The id of an existing Beanstalk environment. 
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>beanstalk_<wbr>environment_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of an existing Beanstalk environment.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>deployment_<wbr>preferences</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#beanstalkdeploymentpreferences">Dict[Beanstalk<wbr>Deployment<wbr>Preferences]</a></span>
    </dt>
    <dd>{{% md %}}Preferences when performing a roll
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>desired_<wbr>capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The desired number of instances the group should have at any time.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>instance_<wbr>types_<wbr>spots</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}One or more instance types. To maximize the availability of Spot instances, select as many instance types as possible.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>maintenance</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>managed_<wbr>actions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#beanstalkmanagedactions">Dict[Beanstalk<wbr>Managed<wbr>Actions]</a></span>
    </dt>
    <dd>{{% md %}}Managed Actions parameters
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max_<wbr>size</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The maximum number of instances the group should have at any time.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>min_<wbr>size</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The minimum number of instances the group should have at any time.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The group name.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>product</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Operation system type. Valid values: `"Linux/UNIX"`, `"SUSE Linux"`, `"Windows"`.
For EC2 Classic instances:  `"Linux/UNIX (Amazon VPC)"`, `"SUSE Linux (Amazon VPC)"`, `"Windows (Amazon VPC)"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>region</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The AWS region your group will be created in. Cannot be changed after the group has been created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>scheduled_<wbr>tasks</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#beanstalkscheduledtask">List[Beanstalk<wbr>Scheduled<wbr>Task]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}










## Supporting Types

<h4>Beanstalk<wbr>Deployment<wbr>Preferences</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/spotinst/types/input/#BeanstalkDeploymentPreferences">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/spotinst/types/output/#BeanstalkDeploymentPreferences">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-spotinst/sdk/go/spotinst/aws?tab=doc#BeanstalkDeploymentPreferencesArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-spotinst/sdk/go/spotinst/aws?tab=doc#BeanstalkDeploymentPreferencesOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Automatic<wbr>Roll</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Should roll perform automatically
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Batch<wbr>Size<wbr>Percentage</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Percent size of each batch
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Grace<wbr>Period</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Amount of time to wait between batches
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Strategies</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#beanstalkdeploymentpreferencesstrategy">List&lt;Beanstalk<wbr>Deployment<wbr>Preferences<wbr>Strategy<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}Strategy parameters
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Automatic<wbr>Roll</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Should roll perform automatically
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Batch<wbr>Size<wbr>Percentage</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Percent size of each batch
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Grace<wbr>Period</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Amount of time to wait between batches
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Strategies</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#beanstalkdeploymentpreferencesstrategy">[]Beanstalk<wbr>Deployment<wbr>Preferences<wbr>Strategy</a></span>
    </dt>
    <dd>{{% md %}}Strategy parameters
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>automatic<wbr>Roll</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Should roll perform automatically
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>batch<wbr>Size<wbr>Percentage</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Percent size of each batch
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>grace<wbr>Period</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Amount of time to wait between batches
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>strategies</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#beanstalkdeploymentpreferencesstrategy">Beanstalk<wbr>Deployment<wbr>Preferences<wbr>Strategy[]?</a></span>
    </dt>
    <dd>{{% md %}}Strategy parameters
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>automatic<wbr>Roll</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Should roll perform automatically
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>batch<wbr>Size<wbr>Percentage</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Percent size of each batch
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>grace_<wbr>period</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Amount of time to wait between batches
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>strategies</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#beanstalkdeploymentpreferencesstrategy">List[Beanstalk<wbr>Deployment<wbr>Preferences<wbr>Strategy]</a></span>
    </dt>
    <dd>{{% md %}}Strategy parameters
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Beanstalk<wbr>Deployment<wbr>Preferences<wbr>Strategy</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/spotinst/types/input/#BeanstalkDeploymentPreferencesStrategy">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/spotinst/types/output/#BeanstalkDeploymentPreferencesStrategy">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-spotinst/sdk/go/spotinst/aws?tab=doc#BeanstalkDeploymentPreferencesStrategyArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-spotinst/sdk/go/spotinst/aws?tab=doc#BeanstalkDeploymentPreferencesStrategyOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Action</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Action to take
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Should<wbr>Drain<wbr>Instances</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Bool value if to wait to drain instance 
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Action</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Action to take
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Should<wbr>Drain<wbr>Instances</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Bool value if to wait to drain instance 
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>action</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Action to take
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>should<wbr>Drain<wbr>Instances</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Bool value if to wait to drain instance 
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>action</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Action to take
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>should<wbr>Drain<wbr>Instances</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Bool value if to wait to drain instance 
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Beanstalk<wbr>Managed<wbr>Actions</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/spotinst/types/input/#BeanstalkManagedActions">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/spotinst/types/output/#BeanstalkManagedActions">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-spotinst/sdk/go/spotinst/aws?tab=doc#BeanstalkManagedActionsArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-spotinst/sdk/go/spotinst/aws?tab=doc#BeanstalkManagedActionsOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Platform<wbr>Update</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#beanstalkmanagedactionsplatformupdate">Beanstalk<wbr>Managed<wbr>Actions<wbr>Platform<wbr>Update<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Platform Update parameters
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Platform<wbr>Update</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#beanstalkmanagedactionsplatformupdate">*Beanstalk<wbr>Managed<wbr>Actions<wbr>Platform<wbr>Update</a></span>
    </dt>
    <dd>{{% md %}}Platform Update parameters
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>platform<wbr>Update</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#beanstalkmanagedactionsplatformupdate">Beanstalk<wbr>Managed<wbr>Actions<wbr>Platform<wbr>Update?</a></span>
    </dt>
    <dd>{{% md %}}Platform Update parameters
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>platform<wbr>Update</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#beanstalkmanagedactionsplatformupdate">Dict[Beanstalk<wbr>Managed<wbr>Actions<wbr>Platform<wbr>Update]</a></span>
    </dt>
    <dd>{{% md %}}Platform Update parameters
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Beanstalk<wbr>Managed<wbr>Actions<wbr>Platform<wbr>Update</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/spotinst/types/input/#BeanstalkManagedActionsPlatformUpdate">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/spotinst/types/output/#BeanstalkManagedActionsPlatformUpdate">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-spotinst/sdk/go/spotinst/aws?tab=doc#BeanstalkManagedActionsPlatformUpdateArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-spotinst/sdk/go/spotinst/aws?tab=doc#BeanstalkManagedActionsPlatformUpdateOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Perform<wbr>At</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Actions to perform (options: timeWindow, never)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Time<wbr>Window</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Time Window for when action occurs ex. Mon:23:50-Tue:00:20
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Update<wbr>Level</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}- Level to update
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Perform<wbr>At</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Actions to perform (options: timeWindow, never)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Time<wbr>Window</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Time Window for when action occurs ex. Mon:23:50-Tue:00:20
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Update<wbr>Level</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}- Level to update
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>perform<wbr>At</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Actions to perform (options: timeWindow, never)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>time<wbr>Window</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Time Window for when action occurs ex. Mon:23:50-Tue:00:20
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>update<wbr>Level</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}- Level to update
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>perform<wbr>At</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Actions to perform (options: timeWindow, never)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>time<wbr>Window</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Time Window for when action occurs ex. Mon:23:50-Tue:00:20
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>update<wbr>Level</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}- Level to update
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Beanstalk<wbr>Scheduled<wbr>Task</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/spotinst/types/input/#BeanstalkScheduledTask">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/spotinst/types/output/#BeanstalkScheduledTask">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-spotinst/sdk/go/spotinst/aws?tab=doc#BeanstalkScheduledTaskArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-spotinst/sdk/go/spotinst/aws?tab=doc#BeanstalkScheduledTaskOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Adjustment</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Adjustment<wbr>Percentage</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Batch<wbr>Size<wbr>Percentage</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Percent size of each batch
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cron<wbr>Expression</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Frequency</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Grace<wbr>Period</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Amount of time to wait between batches
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Is<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Min<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Scale<wbr>Max<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Scale<wbr>Min<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Scale<wbr>Target<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Start<wbr>Time</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Target<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Task<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Adjustment</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Adjustment<wbr>Percentage</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Batch<wbr>Size<wbr>Percentage</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Percent size of each batch
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cron<wbr>Expression</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Frequency</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Grace<wbr>Period</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Amount of time to wait between batches
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Is<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Min<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Scale<wbr>Max<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Scale<wbr>Min<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Scale<wbr>Target<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Start<wbr>Time</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Target<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Task<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>adjustment</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>adjustment<wbr>Percentage</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>batch<wbr>Size<wbr>Percentage</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Percent size of each batch
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cron<wbr>Expression</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>frequency</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>grace<wbr>Period</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Amount of time to wait between batches
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>is<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>min<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>scale<wbr>Max<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>scale<wbr>Min<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>scale<wbr>Target<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>start<wbr>Time</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>target<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>task<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>adjustment</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>adjustment<wbr>Percentage</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>batch<wbr>Size<wbr>Percentage</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Percent size of each batch
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cron<wbr>Expression</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>frequency</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>grace_<wbr>period</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Amount of time to wait between batches
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>is<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>min<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>scale<wbr>Max<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>scale<wbr>Min<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>scale<wbr>Target<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>start<wbr>Time</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>target<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>task<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}









<h3>Package Details</h3>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-spotinst">https://github.com/pulumi/pulumi-spotinst</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
    
</dl>
