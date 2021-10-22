---
description: This page describes a trait/attribute for an NFT
---

# Trait

## Signature

```javascript
export interface Trait {
    traitType?: string;
    value?: string;
    displayType?: string;
    traitCount?: string;
}
```

## Parameters

| Parameter     | Required | Type     | Description                                |
| ------------- | -------- | -------- | ------------------------------------------ |
| `traitType`   | `False`  | `String` | The type of the trait, ex: boost           |
| `value`       | `False`  | `String` | The value of the trait, ex: 5              |
| `displayType` | `False`  | `String` | Chain the transaction will be executed on. |
| `traitCount`  | `False`  | `String` | The number of items having the trait       |
