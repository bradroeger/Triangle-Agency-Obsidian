<%*
const name = await tp.system.prompt("Player character name");
const reality = await tp.system.prompt("Reality");
const anomaly = await tp.system.prompt("Anomaly");
const competency = await tp.system.prompt("Competency");
const slug = value => value.trim().toLowerCase().replace(/[^a-z0-9]+/g, "-").replace(/^-|-$/g, "") || "unspecified";
await tp.file.rename(name);
tR += `---
type: player
player_name: ${JSON.stringify(name)}
reality: ${JSON.stringify(reality)}
anomaly: ${JSON.stringify(anomaly)}
competency: ${JSON.stringify(competency)}
tags:
  - player
  - reality/${slug(reality)}
  - anomaly/${slug(anomaly)}
  - competency/${slug(competency)}
---

# ${name}

## At a glance
- **Reality:** ${reality}
- **Anomaly:** ${anomaly}
- **Competency:** ${competency}
- **Pronouns:**
- **Gender:**
- **Sexual identity:**
- **Age:**

## Character
- **Appearance:**
- **Personality:**
- **Goals:**
- **Secrets:**

## Bonds
- **Bond NPC 1:** [[]]
- **Bond NPC 2:** [[]]

## GM notes
- **Player:**
- **Session notes:**
`;
%>
