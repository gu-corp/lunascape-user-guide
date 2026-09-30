# Connect an external AI (MCP)

**Settings** > **AI Integration** lets an AI assistant outside the browser drive Lunascape through an MCP server. AI clients that speak MCP — Claude Code, Claude Desktop, Cursor, VS Code and others — can read and operate pages in the tabs you already have open, signed in as you are. No extension is needed.

The **AI Integration** page has three tabs: **Tool permissions**, **MCP** and **Audit log**. The MCP server is set up on the **MCP** tab. **Tool permissions** is for the AI sidebar built into Lunascape, and is separate from what MCP clients may do.

## Turn it on

On the **MCP** tab, switch on **Enable MCP server** to start listening. The port is shown while it runs. It is off until you turn it on.

## Choose what it may do

Permissions are granted one at a time under **Permissions** on the **MCP** tab. Turn on only what you need.

| Permission | What it allows |
| --- | --- |
| Read / edit bookmarks | Read bookmarks, and add or change them |
| Read open tabs | List the tabs you have open |
| Open, close and switch tabs | Control tabs |
| Navigate pages (URL, back/forward) | Send a tab to an address |
| Read page content | Read the page being shown |
| Interact with page (click, type, etc.) | Operate elements on the page |
| Read browsing history | Read your history |
| Read downloaded files | Read the contents of files you downloaded |
| Open downloaded files | Open a file in its default application — confirmed every time |
| Read debug data | Read a page's console output, network requests and screenshots |

> **Note:** Opening a file asks for confirmation on every attempt. Allow it only when it matches something you asked for.

## Connect your AI client

**Connection** shows the **Server URL** and **Access token** to connect with. Under **Setup**, pick the AI client you use and a ready-to-paste configuration appears. Copy it and add it to your AI client.

| AI client | Where it goes |
| --- | --- |
| Claude Code | Run the command shown in a terminal |
| Claude Desktop | Add it to the config file (requires Node.js `npx`) |
| Cursor | Add it to `~/.cursor/mcp.json` |
| VS Code | Add it to the project's `.vscode/mcp.json` |
| Anything else | Add the **Generic JSON** to that client's MCP settings |

For Claude Code the command looks like this. Use the URL and token shown on screen.

```sh
claude mcp add --transport http lunascape http://127.0.0.1:7332/mcp --header "Authorization: Bearer <access token>"
```

> **Note:** The access token is the key to operating Lunascape. Do not share it or paste it anywhere public. If you think it has leaked, press **Regenerate token** — the old token stops working at once. Then paste the new configuration into your AI client.

## See what it did

The **Audit log** records every tool the AI called, with what it asked for and what came back. **Entries to keep** sets how much is kept, and **Export CSV** writes it out.

## Restore your bookmarks

Before an AI changes your bookmarks, the whole bookmark tree is saved automatically. Under **Backups**, pick one of the last five and **Restore** it.

## Limit how much is read

**Max characters per file read** caps how much of a file is handed to the AI. Long documents cost more to process, so this is the setting to turn down.

## How it stays safe

- The MCP server accepts connections only from your own computer (`127.0.0.1`). Other computers cannot reach it
- Every connection needs the access token
- The AI can do only what you have granted

> **Tip:** What an AI client does with what it receives from Lunascape is up to that client — usually it is sent to the AI service to produce a reply. When you have a page open that you would rather not share, switch the MCP server off or do not grant reading page content.
