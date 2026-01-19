# Walkthrough: Running Agentic AI Locally on your Machine (GNU/Linux and Mac)

[Github Repo](https://github.com/starship-droid/local-agentic-mcp-workshop/)    [View Slides](to_be_added)    [JanAI Quickstart](https://www.jan.ai/docs/desktop/quickstart)

# Getting Started

## **Prerequisites for JanAI**

- Minimum specs for a decent experience:  
  - 8GB RAM for 3B models  
  - 16GB for 7B  
  - 32GB for 13B  
- Linux: Most distributions work, GPU acceleration available  
  - This walkthrough covers Debian(Ubuntu) step by step  
- macOS: 13.6+ 

## **Installing JanAI**

1. Go to JanAI website  
   [https://www.jan.ai/](https://www.jan.ai/)   
2. Download for your device

### macOS

3. Open the downloaded *.dmg* file   
4. Drag the **Jan** icon to the **Applications** icon  
5. Go to **Applications** and open **Jan**   
   If a warning displays, select **Open**

### Debian / Ubuntu / Mint / Pop\!\_OS users

3. Open your file manager and double-click the .deb file  
4. Click Install  
5. After installation, open Jan from your application menu

### All other Linux distros (Fedora, Arch, Manjaro, openSUSE, etc.)

There is no .rpm or .pkg.tar.zst package yet, so use the AppImage, which works on every Linux system.

3. From JanAI, download the file ending with: “.AppImage”  
4. Make it executable  
   1. Open your terminal in the download folder:  
      cd \~/Downloads  
      chmod \+x Jan\*.AppImage  
5. Run JanAI  
   ./Jan\*.AppImage  
   (You can also double-click it in your file manager once it’s executable.)

## **Getting Models** 

6. Go to the **Hub**  
7. Find a compatible model and select **Download**

## **Starting a Chat**

8. From the **Hub** click **Use** on a downloaded model  
   Or go to **New Chat** from side bar  
9. Models will be pre-selected, you can change a model by clicking on model name

## **Enabling Filesystem MCP Server**

10. Go to Settings then MCP Servers and toggle on the **Allow MCP Tools All Permissions**  
11. Scroll down to **Filesystem** MCP and click on the **Edit** icon  
12. Replace *“/path/to/other/allowed/dir”* with the directory you would like allowed  
13. **Save** and toggle on Filesystem  
    If an error appears, it is usually because an invalid path has been entered.  
14. If successful, a wrench icon will show in a chat  
    Note: Not all models are able to use MCP servers

# Examples MCP Uses

Summarise Meeting Minutes

1. In the github repository, download the meeting_minutes.md file  
   Note: Make sure the file is the downloaded in the directory that the Filesystem MCP is allowed  
2. In a new chat, ask the LLM to summarise the meeting minutes (and you can aks it to put the summary in a new document)

Sample Prompt:  
I missed the meeting.  
Read the file `meeting_minutes.md`.  
Extract only the parts relevant to the **Data team** (data engineering, data science, metrics, pipelines, schemas, analytics), even if they are mixed with frontend or backend discussions.  
**Write the result to a new file called**  
**`data_team_summary.md`** as a concise, structured summary  
using bullet points and short sections.