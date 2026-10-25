<%*
const name = await tp.system.prompt("Anomaly name");
await tp.file.rename(name);
tR += `---
type: anomaly
tags:
  - anomaly
---

# ${name}

## What agents notice
- **Tell / sign:**
- **Effect:**
- **Trigger:**

## GM reference
- **Limits / cost:**
- **Counterplay / containment:**
- **Escalation:**
- **Linked player or NPC:** [[]]
- **Truth / reveal:**
`;
%>
