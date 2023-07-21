---
title: "ConfigurableOperationDefOptions"
weight: 10
date: 2023-07-21T07:16:59.941Z
showtoc: true
generated: true
---
<!-- This file was generated from the Vendure source. Do not modify. Instead, re-run the "docs:build" script -->
import MemberInfo from '@site/src/components/MemberInfo';
import GenerationInfo from '@site/src/components/GenerationInfo';
import MemberDescription from '@site/src/components/MemberDescription';


## ConfigurableOperationDefOptions

<GenerationInfo sourceFile="packages/core/src/common/configurable-operation.ts" sourceLine="230" packageName="@vendure/core" />

Common configuration options used when creating a new instance of a
<a href='/docs/reference/typescript-api/configurable-operation-def/#configurableoperationdef'>ConfigurableOperationDef</a> (

```ts title="Signature"
interface ConfigurableOperationDefOptions<T extends ConfigArgs> extends InjectableStrategy {
  code: string;
  args: T;
  description: LocalizedStringArray;
}
```
* Extends: <code><a href='/docs/reference/typescript-api/common/injectable-strategy#injectablestrategy'>InjectableStrategy</a></code>



<div className="members-wrapper">

### code

<MemberInfo kind="property" type="string"   />

A unique code used to identify this operation.
### args

<MemberInfo kind="property" type="T"   />

Optional provider-specific arguments which, when specified, are
editable in the admin-ui. For example, args could be used to store an API key
for a payment provider service.

*Example*

```ts
args: {
  apiKey: { type: 'string' },
}
```

See <a href='/docs/reference/typescript-api/configurable-operation-def/config-args#configargs'>ConfigArgs</a> for available configuration options.
### description

<MemberInfo kind="property" type="<a href='/docs/reference/typescript-api/configurable-operation-def/localized-string-array#localizedstringarray'>LocalizedStringArray</a>"   />

A human-readable description for the operation method.


</div>