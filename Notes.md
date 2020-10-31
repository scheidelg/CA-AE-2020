**Create OneNote Notebook, Domain, and Redirect**

1. Assign:

    - a name for the class OneNote notebook that is fairly simple and easy to remember
    - a corresponding FQDN as a subdomaon of scheidel.net
    - a corresponding GitHub project name

   We're looking for a OneNote notebook name that's easy for students to remember and closely associated with the event, with a matching FQDN that is easy to remember, short, and easy to type.

   The GitHub project name should be similar to the FQDN but this isn't too important since students won't generally see it.

   For example, for SEC530 at the SANS Cyber Architecture in the United Arab Emirates (AE) I picked:

    - a OneNote notebook name of `SEC530 - CA 2020 AE`
    - an FQDN of `ca2020ae.scheidel.net`
    - a GitHub project name of `SEC530-CA-2020-AE`

1. Create a OneNote notebook with the assigned name.

    - Open OneDrive
    - Browse to the folder containing class OneNote projects
    - Copy the emplate to a new project

1. Update sharing and editing access, and get the page's sharable URL.

   Note: For the time being we're trying to avoid using a shared editing password. We might have to staring using passwords if there are ever problems with people maliciously mucking with the notebook.

    - Access the notebook via OneNote on the web
    - In the top-right corner, click on **Share**
    - Click on **Anyone with the link can edit**
    - Set an expiration date (a few weeks after the class) and click **Apply**
    - Click on **Copy link** to get a shareable link; copy to clipboard; save in a scratchpad so you don't lose it
    - Close the dialog

 1. Create a new GitHub project with GitHub Pages enabled.

     - Open GitHub
     - Create a new GitHub project with the assigned GitHub project name
     - Click on **Settings**
     - Scroll down to the **GitHub Pages** section
     - Change the GitHub Pages **Source** setting to the main branch; click **Save**
     - Change the GitHub Pages **Custom domain** setting to the assigned FQDN; click **Save**

 1. Set up the initial GitHub content with a copy of this `Readme.md` file and an `index.html` file.

    The `index.html` file contents should be similar to:

        <!-- Redirect to the OneNote page for this class -->
        <!DOCTYPE html>
        <html>
          <head>
            <meta http-equiv="Refresh" content="0; url=https://1drv.ms/u/s!AmX2EQD23qhmhiXBpPAESwlyJtrr?e=aIeDSa" />
          </head>
          <body>
            <p>Click to access <a href="https://1drv.ms/u/s!AmX2EQD23qhmhiXBpPAESwlyJtrr?e=aIeDSa">the OneNote page</a> for SEC530 at SANS Cyber Architecture 2020, AE.</p>
          </body>
        </html>

    Edit the `index.html` file contents to use the correct URL in the HTTP redirect and the HREF; and an appropriate label for the OneNote notebook. 

    Note that there will already be a CNAME file. This was automatically created when the custom domain was enabled for GitHub Pages.

 1. Login to GoDaddy and create a CNAME record that redirects to the GitHub project's GitHub Pages web page.
 
     - **Manage My Products**
     - Under the list of domains, find `scheidel.net`
     - To the right of **scheidel.net**, click on **DNS**
     - Click **ADD** to add a new DNS record

| Type | Host | Points to | TTL |
| :--- | :--- | :--- | :--- |
| CNAME | (base name within `scheidel.net`) | scheidelg.github.io | 1 week |

Note: This assumes that we already have the A records created for the apex domain (i.e., `scheidel.net`) to resolve to the GitHub Pages IP addresses:

| Type | Name | Value | TTL |
| :--- | :--- | :--- | :--- |
| A | @ | 185.199.108.153 | 1 week |
| A | @ | 185.199.109.153 | 1 week |
| A | @ | 185.199.110.153 | 1 week |
| A | @ | 185.199.111.153 | 1 week |

**Setup Initial OneNote Notebook Pages**

Refer to the notes in the OneNote template notebook for customizing and updating for this class.
