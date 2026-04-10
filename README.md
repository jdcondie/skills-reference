# app

Internal tools and dashboards.

## skills-reference.html

Single-file dashboard for browsing Claude Code skills and playbooks. Click any skill to copy `/skill-name` to clipboard. Click any playbook to copy a chained prompt that runs its skills in sequence.

### Features

- Playbooks section with click-to-copy chained prompts
- Color-coded cards by category (skills) and type (playbooks)
- Unified search across skills and playbooks (`/` or `Cmd+K` to focus)
- Grid and list view toggle (persists via localStorage)
- Favorites auto-tracked by usage
- Sticky nav with section jump links

### Run locally

```bash
node -e "const h=require('http'),fs=require('fs');h.createServer((q,r)=>{fs.readFile('./skills-reference.html',(e,d)=>{r.writeHead(e?500:200,{'Content-Type':'text/html'});r.end(e?String(e):d);});}).listen(5175,()=>console.log('http://localhost:5175'))"
```
