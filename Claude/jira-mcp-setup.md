
# Claude Code + Atlassian MCP Setup

## Step 1: Open Claude Code

Launch Claude Code in your terminal:

```bash
claude
````

---

## Step 2: Open the MCP Manager

At the Claude Code prompt, run:

```bash
/mcp
```

This opens the MCP (Model Context Protocol) server management dialog.

---

## Step 3: Find the Atlassian Integration

* In the MCP dialog, look for **"atlassian"**
* This is a built-in remote MCP server
* No separate installation is required

---

## Step 4: Authenticate with Atlassian

* Select the **atlassian** entry in the MCP dialog
* Choose **Authenticate** or **Connect**
* A browser window will open (or a URL will be provided)

Then:

* Log in with your Atlassian account (with Jira access)
* Authorize Claude Code to access your data

Return to the terminal. You should see:

```
Authentication successful. Connected to atlassian.
```

---

## Step 5: Verify the Connection

Run:

```bash
claude mcp list
```

You should see something like:

```
atlassian: https://mcp.atlassian.com/v1/mcp (HTTP) - Connected
```

---

## Step 6: Start Using It

Claude can now interact with Jira.

### Examples

* Create a ticket

  ```
  Create a Jira ticket for [description]
  ```

* View open tickets

  ```
  Show me open tickets in a project
  ```

* Update a ticket

  ```
  Update the status of TICKET-123 to In Progress
  ```

* Add a comment

  ```
  Add a comment to TICKET-456
  ```

---

## Notes

* Authentication persists (only needed once per machine)
* Access is limited to your Atlassian permissions
* If disconnected, run `/mcp` again to re-authenticate
* MCP server URL:

  ```
  https://mcp.atlassian.com/v1/mcp
  ```

### Recommendation

Set boundaries for Claude when interacting with Jira.
Example: limit actions to specific projects or workflows as needed.


