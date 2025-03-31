# Mohs Hardness to Durability Chart

This chart establishes a connection between real-world Mohs hardness values and in-game durability for Minecraft tools and armor.

## Overview

The concept leverages in-game materials with well-documented Mohs hardness values from the real world as anchor points. These anchor points (Mohs Hardness, Tool Durability, and Armor Durability Multiplier) remain unchanged, serving as the foundation for mapping other values around them.

### Granularity and Variable Values

To achieve greater granularity, more variable Mohs values were utilized. This approach offered flexibility for Armor Durability Multipliers, especially compared to armors crafted from materials with fixed Mohs values. Since Mohs values can vary significantly, using variable values aligns well with this methodology.

### Vanilla Integration

Known Vanilla values provided a reliable framework, making it straightforward to interpolate the remaining data points. Remarkably, the mapping achieved an **R value of +1**, indicating perfect alignment with the scale derived from Vanilla materials. This ensures high fidelity in translating real-world material properties into gameplay mechanics.

### Durability Scaling

Durability scaling differs based on the type:
- **Tool Durability**: Scales polynomially, reflecting exponential progression.
- **Armor Durability**: Scales linearly, providing a more consistent progression.

### Key Insights

With this chart, the only variable required is the Mohs hardness of the material—whether real or fictional. While the Mohs hardness value itself can be highly conceptual and variable, it serves as the cornerstone for calculating in-game durability.

---

This refined approach combines mathematical precision and creative problem-solving to deliver an intuitive system for modded gameplay progression.

## Detailed Durability Mapping

| Mohs Hardness | Tool Durability | Chest Durability | Multiplier | Material       | Source     |
|---------------|-----------------|------------------|------------|----------------|------------|
| 2.78          | 32              | 112              | 7          | Gold           | Vanilla    |
| 3.06          | 59              | 128              | 8          | Wood           | Vanilla    |
| 3.33          | 82              | 144              | 9          |                |            |
| 3.61          | 108             | 160              | 10         |                |            |
| 3.89          | 131             | 176              | 11         | Stone          | Vanilla    |
| 4.17          | 160             | 192              | 12         |                |            |
| 4.44          | 187             | 208              | 13         |                |            |
| 4.72          | 217             | 224              | 14         |                |            |
| 5.00          | 250             | 240              | 15         | Iron           | Vanilla    |
| 5.28          | 286             | 256              | 16         |                |            |
| 5.56          | 325             | 272              | 17         |                |            |
| 5.83          | 368             | 288              | 18         |                |            |
| 6.11          | 415             | 304              | 19         | Moonstone      | Pure Ores  |
| 6.39          | 466             | 320              | 20         | Fire Opal      | Pure Ores  |
| 6.67          | 522             | 336              | 21         |                |            |
| 6.94          | 582             | 352              | 22         | Jadeite        | Pure Ores  |
| 7.22          | 647             | 368              | 23         |                |            |
| 7.50          | 716             | 384              | 24         | Ametrine       | Pure Ores  |
| 7.78          | 792             | 400              | 25         |                |            |
| 8.06          | 873             | 416              | 26         | Chrysoberyl    | Pure Ores  |
| 8.33          | 957             | 432              | 27         |                |            |
| 8.61          | 1047            | 448              | 28         |                |            |
| 8.89          | 1141            | 464              | 29         | Sapphire       | Pure Ores  |
| 9.17          | 1239            | 480              | 30         |                |            |
| 9.44          | 1342            | 496              | 31         |                |            |
| 9.72          | 1451            | 512              | 32         |                |            |
| 10.00         | 1561            | 528              | 33         | Diamond        | Vanilla    |
| 10.28         | 1670            | 544              | 34         |                |            |
| 10.56         | 1790            | 560              | 35         | Black Diamond  | Pure Ores  |
| 10.83         | 1910            | 576              | 36         |                |            |
| 11.11         | 2031            | 592              | 37         | Netherite      | Vanilla    |
| 11.39         | 2153            | 608              | 38         |                |            |
| 11.67         | 2277            | 624              | 39         |                |            |
| 11.94         | 2401            | 640              | 40         |                |            |
| 12.22         | 2526            | 656              | 41         | Lonsdaleite    | Pure Ores  |

## Graphical Representations

Below are graphical representations of the durability mappings for tools and armor, illustrating the relationships and progression:

![Tool Durability Mapping](infographics/tools.png)

*Figure 1: Tool durability scaling based on Mohs hardness.*

![Armor Durability Mapping](infographics/armor.png)

*Figure 2: Armor durability scaling based on Mohs hardness.*

## Fun Facts and Insights

### Mohs Hardness
- The Mohs hardness values are derived using Vanilla values as anchor points and are scaled against the armor durability multipliers.
- Since real-world materials can exhibit a wide range of Mohs hardness values, whereas the multiplier must be an integer, the Mohs value emerged as the most logical variable for scaling.
- **Calculation**: Mohs Hardness = `((Multiplier + 3) / 3.6)`

### Tool Durability
- Tool durability is calculated using the Mohs hardness value with an exponential formula, allowing for polynomial scaling:
- **Calculation**: Durability = `13.18 × e^(0.425 × Mohs)`

### Armor Durability
- Armor durability is calculated as **Multiplier × 16** for the chestplate. Other armor pieces scale based on different constants:
  - **Head**: Multiplier × 11
  - **Legs**: Multiplier × 15
  - **Feet**: Multiplier × 13
- The chestplate was chosen to represent durability because it has the highest value, and 16 is just a good number.

### Multiplier
- The multiplier directly determines the durability of armors and is explicitly defined in Minecraft's hard-coded Vanilla system.
- Its interpretation is fixed, aligning with the mechanics of the game's core design.

---
