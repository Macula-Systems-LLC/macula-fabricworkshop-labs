# Macula Microsoft Fabric Workshop

Hands-on labs for **Macula's Microsoft Fabric Workshop**. You build a working Fabric platform in your own workspace: a lakehouse, pipelines and dataflows, Spark and Delta tables, a semantic model, and Copilot and data agents.

Please complete the setup below **before the session**. It takes about 10 minutes.

## What you need

- A laptop with a modern browser (Microsoft Edge or Google Chrome). You do not need to install any software.
- A Microsoft Fabric account that you can sign in to with a work or school account, with access to a paid or trial capacity. If you don't have one, you can start a free Fabric trial: https://learn.microsoft.com/fabric/get-started/fabric-trial
- **For Labs 7 and 8 (Copilot and data agents):** a **paid** Fabric capacity with Copilot enabled. If you only have a trial capacity, you can still complete Labs 1 to 6, and Labs 7 and 8 will be shown as demos. If you are unsure whether Copilot is enabled for your tenant, ask your Fabric administrator before the session.

## Step 1: Create a workspace

1. Go to https://app.fabric.microsoft.com and sign in with your Fabric credentials.
1. In the left menu, select **Workspaces**.
1. Create a new workspace and name it `Macula-FabricDemo-Workshop` so it is easy to find.
1. Under **Advanced**, choose a licensing mode that includes Fabric capacity: **Trial**, **Premium**, or **Fabric**.
1. When the workspace opens, it should be empty.

## Step 2: Create a lakehouse

1. In the left menu, select **Create**. If **Create** isn't pinned, select the ellipsis (**...**) first.
1. Under **Data Engineering**, select **Lakehouse** and name it `MaculaWorkshopDemo`.
1. Leave the **Lakehouse schemas** checkbox **selected**. Lab 2 and Lab 5 use `dbo.` table names that need it.
1. Wait about a minute for the lakehouse to be created.
1. In the Lakehouse explorer, confirm you see two empty folders: **Tables** and **Files**.

## Quick check before you arrive

- [ ] I can sign in at https://app.fabric.microsoft.com
- [ ] I have a workspace named `Macula-FabricDemo-Workshop`
- [ ] It contains a lakehouse named `MaculaWorkshopDemo` with empty **Tables** and **Files** folders
- [ ] I know whether my capacity is paid (needed for Labs 7 and 8) or trial

## The labs

All labs share the same workspace and lakehouse, so each lab starts from the state the previous lab left behind. Do them in order.

| Lab | Topic | Approx. time | Lab guide | Files you need |
| --- | --- | --- | --- | --- |
| 1 | Work with a Fabric lakehouse | 30 min | [01-lakehouse.md](Labs/Lab1/01-lakehouse.md) | `Labs/Lab1/Assets/sales.csv` |
| 2 | Ingest data with a pipeline | 45 min | [02-ingest-pipeline.md](Labs/Lab2/02-ingest-pipeline.md) | None (data comes from a URL) |
| 3 | Create and use Dataflows (Gen2) | 30 min | [03-dataflows-gen2.md](Labs/Lab3/03-dataflows-gen2.md) | None (data comes from a URL) |
| 4 | Analyze data with Apache Spark | 45 min | [04-analyze-spark.md](Labs/Lab4/04-analyze-spark.md) | `Labs/Lab4/Assets/orders` folder |
| 5 | Use Delta tables in Apache Spark | 45 min | [05-delta-lake.md](Labs/Lab5/05-delta-lake.md) | `Labs/Lab5/Assets/products.csv` |
| 6 | Design a semantic model for scale | 30 min | [06-design-semantic-model-scale.md](Labs/Lab6/06-design-semantic-model-scale.md) | `Labs/Lab6/Assets/Create-Sales-Data.ipynb` |
| 7 | Analyze data with Spark and Copilot in notebooks | 30 min | [07-copilot-fabric-notebooks.md](Labs/Lab7/07-copilot-fabric-notebooks.md) | Optional: `Labs/Lab7/Assets/eurostat-notebook.ipynb` |
| 8 | Chat with your data using data agents | 30 min | [08-copilot-fabric-data-agents.md](Labs/Lab8/08-copilot-fabric-data-agents.md) | `Labs/Lab8/Assets/create-dw.txt` |

Labs 7 and 8 need a paid capacity with Copilot enabled (see above).

## After the workshop (homework): clean up

We will not clean up during the session. When you have finished exploring, remove what you created so it stops using capacity.

1. If a notebook is still running, select **Stop session** on the notebook menu to end the Spark session.
2. In the left bar, select your workspace icon to see all of its items.
3. Select **Workspace settings**.
4. In the **General** section, scroll down and select **Remove this workspace**.
5. Select **Delete** to confirm.

## Credits

The lab content is adapted from the Microsoft Learning [mslearn-fabric](https://github.com/MicrosoftLearning/mslearn-fabric) repository and the [dp-data](https://github.com/MicrosoftLearning/dp-data) sample files, both released under the MIT License. The original license is included in [NOTICE-MicrosoftLearning-LICENSE.txt](NOTICE-MicrosoftLearning-LICENSE.txt). The Microsoft Learn modules linked from the original labs are a good place to continue after the workshop.
