# Changing Your Website URL

## Changing your Website URL

When you create your GitHub Pages website for the first time, its URL is decided by your GitHub username, and the name of the repo you've created. For example, if your username is `JacobWG`, and you named your repo `bestcomic`, then the URL for your website will be http://JacobWG.github.io/bestcomic/.

There are two ways to change the URL for your web page:&#x20;

* Change your username or repo name
* Assign a custom domain to your website

### Changing your Username

Changing your username will change the part of the URL right before `.github.io`. It will also change the username you use to log into GitHub, and you will have to relogin to GitHub Desktop.&#x20;

To change it:

1.  Click your icon in the top right corner of any GitHub page, then click **Settings**.&#x20;

    <figure><img src="../.gitbook/assets/change_username01_account.png" alt=""><figcaption></figcaption></figure>

    <figure><img src="../.gitbook/assets/change_username02_settings.png" alt=""><figcaption></figcaption></figure>
2. In the list of options on the left, click **Account**.&#x20;
3.  Click **Change Username**. Follow the steps GitHub gives you to complete the process.&#x20;

    <figure><img src="../.gitbook/assets/change_username03_change.png" alt=""><figcaption></figcaption></figure>

### Changing your Repo Name

Changing the name of your webcomic's repository will change the last part of your URL.&#x20;

To change it:

1.  From the main page of your repository, click **Settings**.&#x20;

    <figure><img src="../.gitbook/assets/change_repo01_settings.png" alt=""><figcaption></figcaption></figure>
2.  The first option in General Settings shows your repo name. Click in the text box, make your desired changes, then click **Rename**.&#x20;

    <figure><img src="../.gitbook/assets/change_repo02_rename.png" alt=""><figcaption></figcaption></figure>

## Moving to a Custom Domain

At some point, you will likely want to host your comic from a custom domain, so your readers don't have to keep going to your github.io URL. Fortunately, GitHub Pages supports this!

### Change your GitHub Pages Settings

1.  From the main page of your repository, click **Settings**.&#x20;

    <figure><img src="../.gitbook/assets/change_repo01_settings.png" alt=""><figcaption></figcaption></figure>
2.  In the list of options on the left, click **Pages**. Find the **Custom domain** entry in the Pages settings.&#x20;

    <figure><img src="../.gitbook/assets/custom_domain02_pages.png" alt=""><figcaption></figcaption></figure>
3.  Fill out the text field for the Custom Domain to match whatever custom domain you want to assign to your website, then click **Save**.&#x20;

    <figure><img src="../.gitbook/assets/custom_domain03_set_domain.png" alt=""><figcaption></figcaption></figure>

The page will reload with a blue banner that says `Custom domain "<domain name>" saved.`

### Create a CNAME Record for your Domain

You'll need to set up a CNAME record in the DNS settings of your domain registrar's management page. The exact instructions depend on which registrar you've registered your domain with and is beyond the scope of this article. Most registrars will have their own help documentation telling you how to do this.

GitHub provides more detail on CNAME and other DNS records and what values to enter for them. See [Managing a custom domain for your GitHub Pages site](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site#dns-records-for-your-custom-domain).

### Create a CNAME file in your Repository

In your repository, create a new file called `CNAME` with no extension. In the file, add only a single line with your new domain, e.g. `www.bestcomic.com`&#x20;

#### How do I make a file with no file extension?

Windows by default makes it difficult to create files with no file extension. This section will walk you through a simple method to do so, but any method will work.

First, open File Explorer and go to the View tab, and check the box "File name extensions".

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

Then, go to your repository. Right-click anywhere in the background of the folder, and go to New > Text Document.

<figure><img src="../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

This will create a new text document in your folder and highlight the name to let you change it.

<figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

Select the whole filename, including the `.txt` extension, and replace it with `CNAME` and hit enter. A dialog will pop up warning you that the file "might become unusable". This is normal, and you can finish renaming the file by clicking **Yes**.

The CNAME file has now been created, and it should look like below.

<figure><img src="../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

Now, open the file so you can add your domain by right-clicking the file and clicking **Open with.**

<figure><img src="../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

In the new dialog that pops up, select **Notepad** and click **OK**.

<figure><img src="../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

This will open the file in Notepad. Add only a single line with your new domain, e.g. `www.bestcomic.com`&#x20;

Save and close Notepad, then commit and push your new CNAME file up to your repo. Your website will rebuild and deploy, and should now be accessible from your custom domain!
