# NFT Attributes

## General

The attributes of an NFT item are grouped into three types. 

* property
* stat
* boost

Each type has its own place in the marketplace, and each type has its own display characteristics.

![](../.gitbook/assets/image%20%283%29.png)

### Properties

The properties section is mostly used to display text-based attributes such as the type or category of an item, a team, certain year, rarity, ...

![](../.gitbook/assets/image%20%285%29.png)

### Stats

The stats section is used to display certain stats and metrics, such as the level of a certain item, the amount of defense, power, or top speed a certain item possesses.

When a stat also has a max value defined it will be visualized as a progress bar, otherwise, it will be shown as a card.

![](../.gitbook/assets/image%20%287%29.png)

### Boosts

Boosts is a category to display gains that are achieved by possessing or using a certain item. It usually is accompanied by a positive or negative identifier. Examples of a boost are the increase or decrease of speed, armor but equally, it can be a reduction of certain fees or an increase in chance.

![](../.gitbook/assets/image%20%284%29.png)



## Data Structure

### Signature

```java
"attributes": [
    {
      "type": "property",
      "name": string, 
      "value": string
    }, 
    {
      "type": "stat",
      "name": string, 
      "value": string,
      "maxValue": string
    }, 
    {
      "type": "stat",
      "name": string, 
      "value": string,
    },
    {
      "type": "boost",
      "name": string, 
      "value": string
    }
]

```

### Example

```java
"attributes": [
    {
      "type": "property",
      "name": "Type", 
      "value": "Hero"
    }, 
    {
      "type": "property",
      "name": "Team", 
      "value": "Avengers"
    },
    {
      "type": "stat",
      "name": "Level", 
      "value": "7"
    }, 
    {
      "type": "stat",
      "name": "Strength", 
      "value": "88",
      "maxValue": "93"
    }, 
    {
      "type": "stat",
      "name": "Speed", 
      "value": "74",
      "maxValue": "100"
    },
    {
      "type": "boost",
      "name": "Defence", 
      "value": "+5"
    }, 
    {
      "type": "boost",
      "name": "Rage", 
      "value": "-5"
    }
]
```
