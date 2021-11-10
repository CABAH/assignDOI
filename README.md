# Assign a permanent DOI to your data and code

(originally published on <a href="https://conservationbytes.com/2021/11/02/want-a-permanent-doi-assigned-to-your-data-and-code-follow-this-simple-recipe/#more-211775">ConservationBytes.com</a>)

These days with data and code often required to be designated as open-source, licenced, and fully trackable for most manuscript submissions to a peer-reviewed journal, it’s easy to get lost in the multitude of platforms and options available. In most cases, we no longer have much of a choice to do so, even if you are reticent (although the benefits of posting your data and code online immediately far outweigh any potential disadvantages).

But do you post your data and code on the <a href="https://osf.io/">Open Science Framework</a> (free), <a href="https://github.com/">Github</a> (free), <a href="https://figshare.com/">Figshare</a> (free), <a href="https://zenodo.org/">Zenodo</a> (free, but donations encouraged), <a href="https://datadryad.org/">Dryad</a> ($), or <a href="https://dataverse.harvard.edu/">Harvard Dataverse</a> (free) (and so on, and so on, …)? Pick your favourite. Another issue that arises is that even if you have solved the first dilemma, how do you obtain a <a href="https://www.doi.org/">digital object identifier</a> (DOI) for your data and/or code?

Again, there are many ways to do this, and some methods are more automated than other. That said, I do have a preference that is rather easy to implement that I’d thought I’d share with you here.

## Step 1
The first requirement is getting yourself a (free) Github account. Once you create an account, you can start creating ‘repositories’, which are essentially just sections of your account dedicated to specific code (and data). I mostly code in <a href="https://cran.r-project.org/">R</a>, so I upload my R code text files and associated datasets to these repositories, and spend a good deal of effort on making the <code>Readme.md</code> file highly explanatory and easy to follow. You can check out some of mine <a href="https://github.com/cjabradshaw?tab=repositories">here</a>.

Ok. So, you have a repository with some code and data, you’ve explained what’s going on and how the code works in the Readme file, and now you want a permanent DOI that will point to the repository (and any updates) for all time.

Github doesn’t do this by itself, but it integrates seamlessly with another platform — <a href="http://zenodo.org/">Zenodo</a> — that does. Oh no! Not another platform! Yes, I’m afraid so, but it’s not as painful as you might expect.

## Step 2
Head on over to Zenodo, but don’t create a new account there. Instead, click the <strong>Log in</strong> button on the top right of the page and then choose the option that allows you to login with your Github credentials.

Once you enter this option, you’ll be taken to your Github account to authorise the login through Zenodo. This also authorises what are known as ‘webhooks’ — algorithms that alter the behaviour of a web page with custom callbacks. This essentially means that you’ll allow single identifier (in this case, a DOI) to point to a particular repository in your Github account.

## Step 3
Now click on your account name (upper right) back in Zenodo and choose the <strong>Github</strong> option. This will show a list of all your Github repositories in the linked account. You’ll notice that each repository has a little <strong>OFF</strong> button to to the right of it. Click this to <strong>ON</strong> for the repository for which you want to assign a DOI.

## Step 4
Head back to Github and click on the repository in question. Click <strong>Settings</strong> on the upper right, and then <strong>Webhooks</strong> in the left-side menu. If everything has worked properly, there should be an API (application programming interface) link to Zenodo here.

Back on the main repository view page, find the <strong>Releases</strong> section on the right-hand menu, and click <strong>Create a new release</strong>.

This will give you the option to name your ‘release’, which is usually something along the lines of v1.0.1 (v2.0, etc., etc.). Add a little ‘release’ description in the box below that, and finally a little release note below that (optional). Now click the <strong>Publish release</strong> button. You’re almost finished.

## Step 5
Go back to your Zenodo GitHub page, and there should be a cute, little badge next to your repository showing the new DOI. And yes, if you type doi.org/YOURNEWDOI into any browser, it will now point to a zipped (tarballed) version of your Github repository.

An added bonus is that you can click on the badge itself in Zenodo, and it will provide HTML code that you can place in your Github repository’s Readme file — this will display the badge there too (see one of mine <a href="https://github.com/cjabradshaw/InvasiveSppCostsAustralia">here</a> for an example)!

When you’re ready to submit your manuscript to a journal, all you need to do is provide the DOI and it will point permanently to your Github repository. Lemon squeezie!

<a href="http://github.com/cjabradshaw">CJA Bradshaw</a>
