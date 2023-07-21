---
title: "OrderLineReference"
weight: 10
date: 2023-07-21T07:17:00.940Z
showtoc: true
generated: true
---
<!-- This file was generated from the Vendure source. Do not modify. Instead, re-run the "docs:build" script -->
import MemberInfo from '@site/src/components/MemberInfo';
import GenerationInfo from '@site/src/components/GenerationInfo';
import MemberDescription from '@site/src/components/MemberDescription';


## FulfillmentLine

<GenerationInfo sourceFile="packages/core/src/entity/order-line-reference/fulfillment-line.entity.ts" sourceLine="16" packageName="@vendure/core" />

This entity represents a line from an <a href='/docs/reference/typescript-api/entities/order#order'>Order</a> which has been fulfilled by a <a href='/docs/reference/typescript-api/entities/fulfillment#fulfillment'>Fulfillment</a>.

```ts title="Signature"
class FulfillmentLine extends OrderLineReference {
  constructor(input?: DeepPartial<FulfillmentLine>)
  @Index() @ManyToOne(type => Fulfillment, fulfillment => fulfillment.lines) @Index()
    @ManyToOne(type => Fulfillment, fulfillment => fulfillment.lines)
    fulfillment: Fulfillment;
  @EntityId() @EntityId()
    fulfillmentId: ID;
}
```
* Extends: <code><a href='/docs/reference/typescript-api/entities/order-line-reference#orderlinereference'>OrderLineReference</a></code>



<div className="members-wrapper">

### constructor

<MemberInfo kind="method" type="(input?: DeepPartial&#60;<a href='/docs/reference/typescript-api/entities/order-line-reference#fulfillmentline'>FulfillmentLine</a>&#62;) => FulfillmentLine"   />


### fulfillment

<MemberInfo kind="property" type="<a href='/docs/reference/typescript-api/entities/fulfillment#fulfillment'>Fulfillment</a>"   />


### fulfillmentId

<MemberInfo kind="property" type="<a href='/docs/reference/typescript-api/common/id#id'>ID</a>"   />




</div>


## OrderLineReference

<GenerationInfo sourceFile="packages/core/src/entity/order-line-reference/order-line-reference.entity.ts" sourceLine="15" packageName="@vendure/core" />

This is an abstract base class for entities which reference an <a href='/docs/reference/typescript-api/entities/order-line#orderline'>OrderLine</a>.

```ts title="Signature"
class OrderLineReference extends VendureEntity {
  @Column() @Column()
    quantity: number;
  @Index() @ManyToOne(type => OrderLine, { onDelete: 'CASCADE' }) @Index()
    @ManyToOne(type => OrderLine, { onDelete: 'CASCADE' })
    orderLine: OrderLine;
  @EntityId() @EntityId()
    orderLineId: ID;
}
```
* Extends: <code><a href='/docs/reference/typescript-api/entities/vendure-entity#vendureentity'>VendureEntity</a></code>



<div className="members-wrapper">

### quantity

<MemberInfo kind="property" type="number"   />


### orderLine

<MemberInfo kind="property" type="<a href='/docs/reference/typescript-api/entities/order-line#orderline'>OrderLine</a>"   />


### orderLineId

<MemberInfo kind="property" type="<a href='/docs/reference/typescript-api/common/id#id'>ID</a>"   />




</div>


## OrderModificationLine

<GenerationInfo sourceFile="packages/core/src/entity/order-line-reference/order-modification-line.entity.ts" sourceLine="16" packageName="@vendure/core" />

This entity represents a line from an <a href='/docs/reference/typescript-api/entities/order#order'>Order</a> which has been modified by an <a href='/docs/reference/typescript-api/entities/order-modification#ordermodification'>OrderModification</a>.

```ts title="Signature"
class OrderModificationLine extends OrderLineReference {
  constructor(input?: DeepPartial<OrderModificationLine>)
  @Index() @ManyToOne(type => OrderModification, modification => modification.lines) @Index()
    @ManyToOne(type => OrderModification, modification => modification.lines)
    modification: OrderModification;
  @EntityId() @EntityId()
    modificationId: ID;
}
```
* Extends: <code><a href='/docs/reference/typescript-api/entities/order-line-reference#orderlinereference'>OrderLineReference</a></code>



<div className="members-wrapper">

### constructor

<MemberInfo kind="method" type="(input?: DeepPartial&#60;<a href='/docs/reference/typescript-api/entities/order-line-reference#ordermodificationline'>OrderModificationLine</a>&#62;) => OrderModificationLine"   />


### modification

<MemberInfo kind="property" type="<a href='/docs/reference/typescript-api/entities/order-modification#ordermodification'>OrderModification</a>"   />


### modificationId

<MemberInfo kind="property" type="<a href='/docs/reference/typescript-api/common/id#id'>ID</a>"   />




</div>


## RefundLine

<GenerationInfo sourceFile="packages/core/src/entity/order-line-reference/refund-line.entity.ts" sourceLine="16" packageName="@vendure/core" />

This entity represents a line from an <a href='/docs/reference/typescript-api/entities/order#order'>Order</a> which has been refunded by a {@link Refund}.

```ts title="Signature"
class RefundLine extends OrderLineReference {
  constructor(input?: DeepPartial<RefundLine>)
  @Index() @ManyToOne(type => Refund, refund => refund.lines) @Index()
    @ManyToOne(type => Refund, refund => refund.lines)
    refund: Refund;
  @EntityId() @EntityId()
    refundId: ID;
}
```
* Extends: <code><a href='/docs/reference/typescript-api/entities/order-line-reference#orderlinereference'>OrderLineReference</a></code>



<div className="members-wrapper">

### constructor

<MemberInfo kind="method" type="(input?: DeepPartial&#60;<a href='/docs/reference/typescript-api/entities/order-line-reference#refundline'>RefundLine</a>&#62;) => RefundLine"   />


### refund

<MemberInfo kind="property" type="Refund"   />


### refundId

<MemberInfo kind="property" type="<a href='/docs/reference/typescript-api/common/id#id'>ID</a>"   />




</div>