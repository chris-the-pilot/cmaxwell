+++
date = 2020-06-10T14:42:17Z
title = "Project: CMaxwell.org"

+++
This website, my personal website was setup to have a clean and sleek look with the capabilities of posting a blog. Having a specific CMS platform like WordPress was too much work and maintenance for a simple platform that I didn't want to maintain. On top of that I did not want to run a server because of needing to setup scalable and fault-tolerant infrastructure. Another concern was the security risk putting up a server on LAMP stack would entail meaning I'd have to manage that extra risk. I could of course have gone with another blog platform but I wanted to set this website up as a portfolio project showcasing my infrastructure and DevOps skills, on top of that I also want to own and control my own content. The solution I ended up with was using a serverless static website hosted on S3. The beauty is that I can easily connect a CDN to host my pages with quick load times and because I'm running S3 there is virtually no maintance.

**Summary:**

* Chose **stack** to setup my website
* Implemented **HUGO** as a **SSG (Static Site Generator)**
* Setup **GitHub** repo for SSG and blog content
* Connected Forestry as a **git**-backed CMS
* Built **CI/CD pipeline** using AWS CodePipeline
  * Commits coming from GitHub
  * Build HUGO-site and package the static site generated to be sent to deploy
  * Deploy to **S3-bucket** as a static website
* Setup **static website** hosting on S3
* Connect **R53** domain to work on S3