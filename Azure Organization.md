# What is Azure Organization

Azure organization is the whole structure that holds a company’s stuff in Azure. This structure has layers, like a company. Imagine I own a company called **Arasaka Corp**. To run it I need:

- A company registry that says who works here and who is allowed to do what.
- Departments to group things (Sales, Engineering).
- Credit cards so someone pays for what gets used.
- Project folders to keep related things together.
- The actual stuff: computers, databases, websites.

Azure has exactly these five layers:

<table>
  <tr>
    <th>My company</th>
    <th>Azure Name</th>
    <th>What it really is</th>
  </tr>
  <tr>
    <td>Company Registry</td>
    <td>Tenant (Microsoft Entra ID)</td>
    <td>The list of users and their logins. This is your “organization”.</td>
  </tr>
  <tr>
    <td>Department</td>
    <td>Management Groups</td>
    <td>Optional folders that group subscriptions so you can apply rules to many at once</td>
  </tr>
  <tr>
    <td>Credit cards</td>
    <td>Subscriptions</td>
    <td>The billing container. Everything you create is charged to one.</td>
  </tr>
  <tr>
    <td>Project folders</td>
    <td>Resource Groups</td>
    <td>Folders that hold related things (for example, everything for one app)</td>
  </tr>
  <tr>
    <td>The stuff</td>
    <td>Resources</td>
    <td>A virtual machine, a database, a storage account, a website</td>
  </tr>
</table>

```bash
Tenant (Acme Corp: who are the people?)
 └── Management Group (Engineering Dept)
      └── Subscription (the credit card)
           └── Resource Group (the "Website Project" folder)
                └── Resources (VM, database, storage...)
```
