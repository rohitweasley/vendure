---
title: "HistoryEntry"
weight: 10
date: 2023-07-21T07:17:00.878Z
showtoc: true
generated: true
---
<!-- This file was generated from the Vendure source. Do not modify. Instead, re-run the "docs:build" script -->
import MemberInfo from '@site/src/components/MemberInfo';
import GenerationInfo from '@site/src/components/GenerationInfo';
import MemberDescription from '@site/src/components/MemberDescription';


## HistoryEntry

<GenerationInfo sourceFile="packages/core/src/entity/history-entry/history-entry.entity.ts" sourceLine="14" packageName="@vendure/core" />

An abstract entity representing an entry in the history of an Order (<a href='/docs/reference/typescript-api/entities/order-history-entry#orderhistoryentry'>OrderHistoryEntry</a>)
or a Customer (<a href='/docs/reference/typescript-api/entities/customer-history-entry#customerhistoryentry'>CustomerHistoryEntry</a>).

```ts title="Signature"
class HistoryEntry extends VendureEntity {
  @Index() @ManyToOne(type => Administrator) @Index()
    @ManyToOne(type => Administrator)
    administrator?: Administrator;
  @Column({ nullable: false, type: 'varchar' }) readonly @Column({ nullable: false, type: 'varchar' })
    readonly type: HistoryEntryType;
  @Column() @Column()
    isPublic: boolean;
  @Column('simple-json') @Column('simple-json')
    data: any;
}
```
* Extends: <code><a href='/docs/reference/typescript-api/entities/vendure-entity#vendureentity'>VendureEntity</a></code>



<div className="members-wrapper">

### administrator

<MemberInfo kind="property" type="<a href='/docs/reference/typescript-api/entities/administrator#administrator'>Administrator</a>"   />


### type

<MemberInfo kind="property" type="HistoryEntryType"   />


### isPublic

<MemberInfo kind="property" type="boolean"   />


### data

<MemberInfo kind="property" type="any"   />




</div>