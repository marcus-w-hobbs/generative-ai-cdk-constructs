[**@cdklabs/generative-ai-cdk-constructs**](../../../../README.md)

***

[@cdklabs/generative-ai-cdk-constructs](../../../../README.md) / [bedrock](../README.md) / AgentAlias

# Class: AgentAlias

Class to create an Agent Alias with CDK.

## Cloudformation Resource

AWS::Bedrock::AgentAlias

## Extends

- [`AgentAliasBase`](AgentAliasBase.md)

## Constructors

### Constructor

> **new AgentAlias**(`scope`, `id`, `props`): `AgentAlias`

#### Parameters

##### scope

`Construct`

##### id

`string`

##### props

[`AgentAliasProps`](../interfaces/AgentAliasProps.md)

#### Returns

`AgentAlias`

#### Overrides

[`AgentAliasBase`](AgentAliasBase.md).[`constructor`](AgentAliasBase.md#constructor)

## Properties

### agent

> `readonly` **agent**: [`IAgent`](../interfaces/IAgent.md)

The underlying agent for this alias.

#### Overrides

[`AgentAliasBase`](AgentAliasBase.md).[`agent`](AgentAliasBase.md#agent)

***

### aliasArn

> `readonly` **aliasArn**: `string`

The ARN of the agent alias.

#### Example

```ts
`arn:aws:bedrock:us-east-1:123456789012:agent-alias/DNCJJYQKSU/TCLCITFZTN`
```

#### Overrides

[`AgentAliasBase`](AgentAliasBase.md).[`aliasArn`](AgentAliasBase.md#aliasarn)

***

### aliasId

> `readonly` **aliasId**: `string`

The unique identifier of the agent alias.

#### Example

```ts
`TCLCITFZTN`
```

#### Overrides

[`AgentAliasBase`](AgentAliasBase.md).[`aliasId`](AgentAliasBase.md#aliasid)

***

### aliasName

> `readonly` **aliasName**: `string`

***

### env

> `readonly` **env**: `ResourceEnvironment`

The environment this resource belongs to.
For resources that are created and managed by the CDK
(generally, those created by creating new class instances like Role, Bucket, etc.),
this is always the same as the environment of the stack they belong to;
however, for imported resources
(those obtained from static methods like fromRoleArn, fromBucketName, etc.),
that might be different than the stack they were imported into.

#### Inherited from

[`AgentAliasBase`](AgentAliasBase.md).[`env`](AgentAliasBase.md#env)

***

### node

> `readonly` **node**: `Node`

The tree node.

#### Inherited from

[`AgentAliasBase`](AgentAliasBase.md).[`node`](AgentAliasBase.md#node)

***

### physicalName

> `protected` `readonly` **physicalName**: `string`

Returns a string-encoded token that resolves to the physical name that
should be passed to the CloudFormation resource.

This value will resolve to one of the following:
- a concrete value (e.g. `"my-awesome-bucket"`)
- `undefined`, when a name should be generated by CloudFormation
- a concrete name generated automatically during synthesis, in
  cross-environment scenarios.

#### Inherited from

[`AgentAliasBase`](AgentAliasBase.md).[`physicalName`](AgentAliasBase.md#physicalname)

***

### stack

> `readonly` **stack**: `Stack`

The stack in which this resource is defined.

#### Inherited from

[`AgentAliasBase`](AgentAliasBase.md).[`stack`](AgentAliasBase.md#stack)

## Methods

### \_enableCrossEnvironment()

> **\_enableCrossEnvironment**(): `void`

**`Internal`**

Called when this resource is referenced across environments
(account/region) to order to request that a physical name will be generated
for this resource during synthesis, so the resource can be referenced
through its absolute name/arn.

#### Returns

`void`

#### Inherited from

[`AgentAliasBase`](AgentAliasBase.md).[`_enableCrossEnvironment`](AgentAliasBase.md#_enablecrossenvironment)

***

### applyRemovalPolicy()

> **applyRemovalPolicy**(`policy`): `void`

Apply the given removal policy to this resource

The Removal Policy controls what happens to this resource when it stops
being managed by CloudFormation, either because you've removed it from the
CDK application or because you've made a change that requires the resource
to be replaced.

The resource can be deleted (`RemovalPolicy.DESTROY`), or left in your AWS
account for data recovery and cleanup later (`RemovalPolicy.RETAIN`).

#### Parameters

##### policy

`RemovalPolicy`

#### Returns

`void`

#### Inherited from

[`AgentAliasBase`](AgentAliasBase.md).[`applyRemovalPolicy`](AgentAliasBase.md#applyremovalpolicy)

***

### generatePhysicalName()

> `protected` **generatePhysicalName**(): `string`

#### Returns

`string`

#### Inherited from

[`AgentAliasBase`](AgentAliasBase.md).[`generatePhysicalName`](AgentAliasBase.md#generatephysicalname)

***

### getResourceArnAttribute()

> `protected` **getResourceArnAttribute**(`arnAttr`, `arnComponents`): `string`

Returns an environment-sensitive token that should be used for the
resource's "ARN" attribute (e.g. `bucket.bucketArn`).

Normally, this token will resolve to `arnAttr`, but if the resource is
referenced across environments, `arnComponents` will be used to synthesize
a concrete ARN with the resource's physical name. Make sure to reference
`this.physicalName` in `arnComponents`.

#### Parameters

##### arnAttr

`string`

The CFN attribute which resolves to the ARN of the resource.
Commonly it will be called "Arn" (e.g. `resource.attrArn`), but sometimes
it's the CFN resource's `ref`.

##### arnComponents

`ArnComponents`

The format of the ARN of this resource. You must
reference `this.physicalName` somewhere within the ARN in order for
cross-environment references to work.

#### Returns

`string`

#### Inherited from

[`AgentAliasBase`](AgentAliasBase.md).[`getResourceArnAttribute`](AgentAliasBase.md#getresourcearnattribute)

***

### getResourceNameAttribute()

> `protected` **getResourceNameAttribute**(`nameAttr`): `string`

Returns an environment-sensitive token that should be used for the
resource's "name" attribute (e.g. `bucket.bucketName`).

Normally, this token will resolve to `nameAttr`, but if the resource is
referenced across environments, it will be resolved to `this.physicalName`,
which will be a concrete name.

#### Parameters

##### nameAttr

`string`

The CFN attribute which resolves to the resource's name.
Commonly this is the resource's `ref`.

#### Returns

`string`

#### Inherited from

[`AgentAliasBase`](AgentAliasBase.md).[`getResourceNameAttribute`](AgentAliasBase.md#getresourcenameattribute)

***

### grant()

> **grant**(`grantee`, ...`actions`): `Grant`

Grant the given principal identity permissions to perform actions on this agent alias.

#### Parameters

##### grantee

`IGrantable`

##### actions

...`string`[]

#### Returns

`Grant`

#### Inherited from

[`AgentAliasBase`](AgentAliasBase.md).[`grant`](AgentAliasBase.md#grant)

***

### grantGet()

> **grantGet**(`grantee`): `Grant`

Grant the given identity permissions to get the agent alias.

#### Parameters

##### grantee

`IGrantable`

#### Returns

`Grant`

#### Inherited from

[`AgentAliasBase`](AgentAliasBase.md).[`grantGet`](AgentAliasBase.md#grantget)

***

### grantInvoke()

> **grantInvoke**(`grantee`): `Grant`

Grant the given identity permissions to invoke the agent alias.

#### Parameters

##### grantee

`IGrantable`

#### Returns

`Grant`

#### Inherited from

[`AgentAliasBase`](AgentAliasBase.md).[`grantInvoke`](AgentAliasBase.md#grantinvoke)

***

### onCloudTrailEvent()

> **onCloudTrailEvent**(`id`, `options`): `Rule`

Define an EventBridge rule that triggers when something happens to this agent alias

Requires that there exists at least one CloudTrail Trail in your account
that captures the event. This method will not create the Trail.

#### Parameters

##### id

`string`

The id of the rule

##### options

`OnEventOptions` = `{}`

Options for adding the rule

#### Returns

`Rule`

#### Inherited from

[`AgentAliasBase`](AgentAliasBase.md).[`onCloudTrailEvent`](AgentAliasBase.md#oncloudtrailevent)

***

### toString()

> **toString**(): `string`

Returns a string representation of this construct.

#### Returns

`string`

#### Inherited from

[`AgentAliasBase`](AgentAliasBase.md).[`toString`](AgentAliasBase.md#tostring)

***

### fromAttributes()

> `static` **fromAttributes**(`scope`, `id`, `attrs`): [`IAgentAlias`](../interfaces/IAgentAlias.md)

Brings an Agent Alias from an existing one created outside of CDK.

#### Parameters

##### scope

`Construct`

##### id

`string`

##### attrs

[`AgentAliasAttributes`](../interfaces/AgentAliasAttributes.md)

#### Returns

[`IAgentAlias`](../interfaces/IAgentAlias.md)

***

### isConstruct()

> `static` **isConstruct**(`x`): `x is Construct`

Checks if `x` is a construct.

Use this method instead of `instanceof` to properly detect `Construct`
instances, even when the construct library is symlinked.

Explanation: in JavaScript, multiple copies of the `constructs` library on
disk are seen as independent, completely different libraries. As a
consequence, the class `Construct` in each copy of the `constructs` library
is seen as a different class, and an instance of one class will not test as
`instanceof` the other class. `npm install` will not create installations
like this, but users may manually symlink construct libraries together or
use a monorepo tool: in those cases, multiple copies of the `constructs`
library can be accidentally installed, and `instanceof` will behave
unpredictably. It is safest to avoid using `instanceof`, and using
this type-testing method instead.

#### Parameters

##### x

`any`

Any object

#### Returns

`x is Construct`

true if `x` is an object created from a class which extends `Construct`.

#### Inherited from

[`AgentAliasBase`](AgentAliasBase.md).[`isConstruct`](AgentAliasBase.md#isconstruct)

***

### isOwnedResource()

> `static` **isOwnedResource**(`construct`): `boolean`

Returns true if the construct was created by CDK, and false otherwise

#### Parameters

##### construct

`IConstruct`

#### Returns

`boolean`

#### Inherited from

[`AgentAliasBase`](AgentAliasBase.md).[`isOwnedResource`](AgentAliasBase.md#isownedresource)

***

### isResource()

> `static` **isResource**(`construct`): `construct is Resource`

Check whether the given construct is a Resource

#### Parameters

##### construct

`IConstruct`

#### Returns

`construct is Resource`

#### Inherited from

[`AgentAliasBase`](AgentAliasBase.md).[`isResource`](AgentAliasBase.md#isresource)
