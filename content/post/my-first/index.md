---
title: How the TLPF website is built, and how Nairobi TLPF staff can edit it
date: 2021-01-30
gallery_item:
  - album: gallery
    image: kap.race.2019.png
    caption: A caption
    gallery_item: null
  - album: gallery
    image: National-Cross-Country_Eldoret_9-800x600.jpg
    caption: A caption
    gallery_item: null
  - album: gallery
    image: oneyoungworldsummit.jpg
    caption: A caption
    gallery_item: null
  - album: gallery
    image: purbiel.jpg
    caption: A caption
subtitle: What our Webmaster needs to know
---
### How the **Tegla Loroupe Peace Foundation** website is structured

Editing is in the cloud, supported by our web publishing partner, **Netlify**. That's why our current web address is [https://teglaloroupepeacefoundation.netlify.app](https://teglaloroupepeacefoundation.netlify.app/)/

To access the editor, you log in to **Netlify**.  We'll set that up.

You are presented with *NetlifyCMS*, the content-management system  (CMS) supported by **Netlify**.  The interface displays a form for each page, allowing you to edit the text, the title, and the images displayed on the page.

*NetlifyCMS* is structured by an outline created by **Wowchemy**, a non-profit open source provider of tools to build websites. 

Content is divided into categories: homepage, posts, blogs, slides, books, projects, events, publications, and content, and the categories match the physical arrangement of the directories that hold the content.  That is, each of these categories is a directory inside the overall directory named "content".  For example, all the posts are inside "content/post".  The homepage is inside "content/home". The events are inside "content/events".

Each time we create a new post, for example, the CMS system creates a new folder inside "content/post", with the name of the title of the post, and it puts the text of the post in a file named "index.md", and the images for the post alongside index.md.

**Wowchemy** sometimes refers to the online editing system as "*Wowchemy CMS*", because they designed the structure, the arrangement of directories and folders that hold the content, and the software tools to create the web pages.

#### Here's the overall plan: 

1. Editing content interacts with the pages visible in the *NetlifyCMS*.

2. As content is added or changed, *NetlifyCMS* keeps track. Finally, when you are ready to "Publish", you click on the "Publish" button, and *NetlifyCMS* gathers everything together, and moves it to where is is permanently stored.

3. All content is permanently stored in an independent site, named **Github.** Currently, it's in what's called a **repository** in my account at **Github**, but we will create a TLPF repository, governed by TLPF. It's all free.  Millions of people use **Github** to store all their software. Microsoft bought them a few years ago, and happily have not ruined them.

4. Since all the content is there, you can also edit it using the **Github** editor, which is a different discussion.  Since the **Github** repository is linked to the *NetlifyCMS*, any changes made to the content at **Github** is instantly visible at the *NetlifyCMS*

5. I'm making an outline course for the learning process for our **TLPF Webmaster.** You can get a quick idea from this video that describes what someone needs to know to be able to get a job as a Webmaster.

Here's the video to watch, to get the overall idea of what's needed: [Web Development 2021](https://www.youtube.com/watch?v=VfGW0Qiy2I0&ab_channel=TraversyMedia)

And, as a practical matter, this could be the beginning of a course for the athletes who want to gain skills that can get them jobs.

**Here's a tiny taste of how a page is built**

Write text in the text field for a page.  When you want to insert an image, put in this line, making the appropriate changes to the words inside the double curly brackets: {{ .  }}

The curly brackets are the magical commands that the Wowchemy software looks for to insert images, or create a gallery of photos, or create a link to a Twitter account, or a dozen other things 

*{{< figure library="true" src="tl.logo.png" title="A caption" >}}*
![Tegla logo](/tl.logo.png "Tegla Running")

##### How are images displayed?

The important thing for the Wowchemy software to know is exactly where the image is stored. It might be in the same folder as the text, which is in a file named "index.md", so the "src=tl.logo.png" means the image is there, next to "index.md" , or it might be in a special folder just for images available to all pages, which is why the words 'library="true" 'are inside the curly brackets.