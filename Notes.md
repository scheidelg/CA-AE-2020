1. Assign:

    - a name for the class OneNote notebook that is fairly simple and easy to remember
    - a corresponding FQDN as a subdomaon of scheidel.net
    - a corresponding GitHub project name

   We're looking for a OneNote notebook name that's easy for students to remember and closely associated with the event, with a matching FQDN that is easy to remember, short, and easy to type.

   The GitHub project name should be similar to the FQDN but this isn't super important, since students won't generally see it.

   For example, for SEC530 at the SANS Cyber Architecture in the United Arab Emirates (AE) I picked:

    - a OneNote notebook name of `CA 2020 AE - SEC530`
    - an FQDN of `ca2020ae.scheidel.net`
    - a GitHub project name of `CA-2020-AE`

2. Create a OneNote notebook with the assigned name.

    - Open OneNote on the web
    - Under the list of **My Notebooks**, click **+ New**

3. Update sharing and editing access, and get the page's sharable URL.

   Note: For the time being we're trying to avoid using a shared editing password. We might have to staring using passwords if there are ever problems with people maliciously mucking with the notebook.

    - Access the notebook via OneNote on the web
    - In the top-right corner, click on **Share**
    - Click on **Anyone with the link can edit**
    - Set an expiration date and click **Apply**
    - Click on **Copy link** to get a shareable link; copy to clipboard; save in a scratchpad so you don't lose it
    - Close the dialog

 4. Create a new GitHub project with GitHub Pages enabled.

     - Open GitHub
     - Create a new GitHub project with the assigned GitHub project name
     - Click on **Settings**
     - Scroll down to the **GitHub Pages** section
     - Change the GitHub Pages **Source** setting to the main branch; click **Save**
     - Change the GitHub Pages **Custom domain** setting to the assigned FQDN; click **Save**

 5. Set up the initial GitHub content with a copy of this `Readme.md` file and an `index.html` file.

    The `index.html` file contents should be similar to:

        blah
        blah
        blah

    Edit the `index.html` file contents to use the correct URL in the HTTP redirect and the HREF; and an appropriate label for the OneNote notebook. 

    Note that there will already be a CNAME file. This was automatically created when the custom domain was enabled for GitHub Pages.

 (notes on setting up the OneNote notebook structure
