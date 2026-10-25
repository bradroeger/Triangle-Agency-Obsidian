<%*
const name = await tp.system.prompt("NPC name");
await tp.file.rename(name);
tR += `---
type: npc
tags:
  - npc
---

# ${name}

- **Role / faction:**
- **Wants:**
- **Personality / tell:**
- **Knows:**
- **Location:** [[]]
- **Connected players:** [[]]

## GM notes
`;
%>
