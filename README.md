# Fortnite-shop-guide

> [!IMPORTANT]
> **Find cosmetics:** [Fortnite.GG/Cosmetics](https://fortnite.gg/cosmetics?game=br&type=outfit&season=1,2,3,4,5,6,7,8,9,10,11,12,13,14,15&sort=oldest)
> 
> **Version limit:** Chapter 2 Season 5 (v15.30) and older only

&nbsp;

---

&nbsp;

# Step 1: Understand the Format

> [!WARNING]
> **ALWAYS use double quotes around the ENTIRE cosmetic ID**
>
> Format: `"ItemType:CosmeticID"`

**Examples:**
```json
"AthenaCharacter:CID_259_Athena_Commando_M_StreetOps"
"AthenaDance:EID_FrisbeeShow"
"AthenaPickaxe:Pickaxe_ID_190_GolfClub"
```

&nbsp;

---

&nbsp;

# Step 2: Know Your Item Types

| Cosmetic | Item Type |
|----------|-----------|
| Skins | `AthenaCharacter` |
| Emotes | `AthenaDance` |
| Pickaxes | `AthenaPickaxe` |
| Backblings | `AthenaBackpack` |
| Gliders | `AthenaGlider` |
| Wraps | `AthenaItemWrap` |
| Loading Screens | `AthenaLoadingScreen` |
| Contrails | `AthenaSkyDiveContrail` |

&nbsp;

---

&nbsp;

# Step 3: Fill In Your Shop

Your shop has **10 slots** (6 daily + 4 featured).

Each slot needs:
• **itemGrants** = cosmetic ID in quotes
• **price** = V-Bucks (no commas)

**Template:**
```json
{
  "//": "BR Item Shop Config",
  "daily1": {
      "itemGrants": [""],
      "price": 0
  },
  "daily2": {
      "itemGrants": [""],
      "price": 0
  },
  "daily3": {
      "itemGrants": [""],
      "price": 0
  },
  "daily4": {
      "itemGrants": [""],
      "price": 0
  },
  "daily5": {
      "itemGrants": [""],
      "price": 0
  },
  "daily6": {
      "itemGrants": [""],
      "price": 0
  },

  },
  "daily7": {
      "itemGrants": [""],
      "price": 0
  },

  },
  "daily8": {
      "itemGrants": [""],
      "price": 0
  },

  },
  "daily9": {
      "itemGrants": [""],
      "price": 0
  },

  },
  "daily10": {
      "itemGrants": [""],
      "price": 0
  },

  "featured1": {
      "itemGrants": [""],
      "price": 0
  },
  "featured2": {
      "itemGrants": [""],
      "price": 0
  }

}
  "featured3": {
      "itemGrants": [""],
      "price": 0
  }

}
  "featured4": {
      "itemGrants": [""],
      "price": 0
  }
}

  "featured5": {
      "itemGrants": [""],
      "price": 0
  }
}
```

&nbsp;

---

&nbsp;

# Step 4: See a Complete Example

```json
{
  "//": "BR Item Shop Config",
  "daily1": {"itemGrants": ["AthenaCharacter:CID_259_Athena_Commando_M_StreetOps"], "price": 1200},
  "daily2": {"itemGrants": ["AthenaCharacter:CID_260_Athena_Commando_F_StreetOps"], "price": 1200},
  "daily3": {"itemGrants": ["AthenaPickaxe:Pickaxe_ID_190_GolfClub"], "price": 500},
  "daily4": {"itemGrants": ["AthenaGlider:Glider_ID_176_BlackMondayCape_4P79K"], "price": 800},
  "daily5": {"itemGrants": ["AthenaBackpack:BID_229_LuckyRiderMale"], "price": 750},
  "daily6": {"itemGrants": ["AthenaItemWrap:Wrap_197_ToxinBubbles"], "price": 250},
  "featured1": {"itemGrants": ["AthenaDance:EID_FrisbeeShow"], "price": 500},
  "featured2": {"itemGrants": ["AthenaCharacter:CID_650_Athena_Commando_F_HolidayPJ_B"], "price": 800},
  "featured3": {"itemGrants": ["AthenaCharacter:CID_048_Athena_Commando_F_HolidayGingerbread"], "price": 1500},
  "featured4": {"itemGrants": ["AthenaPickaxe:Pickaxe_ID_015_HolidayCandyCane"], "price": 1500}
}
```

&nbsp;

---

&nbsp;

# Common Mistakes

### ❌ Missing the Format Completely
**People often just write the ID with no format.**

**Wrong:**
```json
"itemGrants": ["CID_259_Athena_Commando_M_StreetOps"]
```

**Right:**
```json
"itemGrants": ["AthenaCharacter:CID_259_Athena_Commando_M_StreetOps"]
```

**You MUST include** `ItemType:` **before the ID!**

&nbsp;

### ❌ Missing Quotes
**The entire ID needs to be in quotes.**

**Wrong:**
```json
"itemGrants": [AthenaCharacter:CID_Example]
```

**Right:**
```json
"itemGrants": ["AthenaCharacter:CID_Example"]
```

&nbsp;

### ❌ Commas in Numbers
**V-Bucks prices cannot have commas.**

**Wrong:**
```json
"price": 1,200
```

**Right:**
```json
"price": 1200
```
