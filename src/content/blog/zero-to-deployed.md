---
title: "From Zero to Deployed in a day!"
description: "How I go from Zero to having my personal website up and running in a day using cloudflare!"
pubDate: "Jul 03 2024"
heroImage: "/blog-placeholder-zero.jpg"
---

## 🌐 From Zero to Deployed: Building a Scalable Website with Astro, Flask & Cloudflare, and automate with Cloudflare Workers.

This repository documents my personal journey of building a full-stack website—starting with zero infrastructure and ending with a fast, secure, and professional site for **Prevalis.AI Strategies**, deployed on **Cloudflare**.

---

### 💡 Backgroud

In the process of learning various technologies, including serverless architecture, I wonder how difficult it would be to host a professional website on Cloudflare and automate content and code update from github. The only way to find out is to **experiment!**

### 🚀 Overview

- **Frontend:** [Astro](https://astro.build/) – clean, fast, and content-friendly
I chose Astro for frontend instead of React or others, since the website will be content-loaded and minimal user interactions.

- **Backend:** [Flask](https://flask.palletsprojects.com/) + [SQLAlchemy Core](https://docs.sqlalchemy.org/core/) – for robust API handling and database persistence
I've worked with Flasks before on small projects, for which it is superb.

- **Deployment:** [Cloudflare](https://www.cloudflare.com/) – secure DNS, routing, and email integration
Comparing various options, including Vercel, I've decided to go with Cloudflare, since it has supports in APAC region, in case I need it in the future. Also their security technologies are superb! Plus it has Compute Workers to help automate a lot of tedious tasks, like content grab and update.

- **Email:** [Proton Mail](https://proton.me/) – for privacy-first, custom-domain communication
Since I don't want to go all-in in setting up Exchange Server, and I already have Proton Unlimited account, I decided to go with Proton. It's focuses on privacy and security are what I look for! 
---

### 🧭 My Milestones

#### 1. ✅ Zero to Static Frontend (Astro)

- Learned Astro’s island architecture and routing system
- Built responsive pages using .astro files and minimal JavaScript
- Implemented blog sorting via Markdown frontmatter (sorted by `date`)

#### 2. ✅ Server-side Power (Flask + SQLAlchemy)

- Built an app.py Flask server for processing form data
- Connected a SQLite database using SQLAlchemy with modularized models and structured logging
- Handled email collection via a POST /submit endpoint (JSON payload)

Simple Server-side with Flask, now in testing and will be deployed later***

#### 3. ✅ Connecting the Dots

- Wrote a lightweight JS fetch client in Astro to send email data to Flask
- Configured CORS so the frontend and backend could communicate across ports and environments
- Validated and sanitized data before persisting

Still in the process of working out a few kinks with this for now***

#### 4. ✅ Going Live with Cloudflare

- Registered prevalis.ai and configured DNS records
Cloudflare also handles domain registration quite nicely, and DNS configurations are quite straightforward.

- Set up Cloudflare Workers to fetch my github repositories
This one is also quite straightforward. Choose the appropriate Cloudflare Workers and connect to (or create) your github repo. Once you code, you can add, commit, and push your code to github, then Cloudflare Workers will handle deployment. Doesn't get any easier than this! 


- Deployed and routed traffic via Cloudflare
This one is a little tricky, as you need to route DNS traffic to Cloudflare Workers, website.user.workers.dev, instead of your website. Took a bit of trial-and-error to figure it out. But once that's done. Everything just works!


- Set up Proton Mail for custom domain email routing
Just go to Proton Mail setting and add your new domain to the list. Setting up is a breeze.
---

And that's it! I started out in the morning, with a goal to experiment with serverless architecture, and ended up in the evening with a professional website running on one! All it costs was the price of a domain name! I'm still using Cloudflare's free tier, which gives you room to play with your site, with DDos protection, WAF, Universal SSL, plus a host of Analytics & Logs. But once the site gets bigger, I will definitely move to their Pro/Business plan.


### 💡 Key Learnings

- Astro is incredibly fast but requires strategic client-side scripting for interactivity
- SQLAlchemy Core gives more explicit control than ORM—ideal for learning and scaling
- Form data handling across frontend-backend boundaries must be secured, structured, and CORS-enabled
- Cloudflare makes DNS, HTTPS, and Workers deployment surprisingly elegant
- Proton handles mails like a champ, with privacy and security as priority! 

---

### 📬 What’s Next
- I still have a lot more to learn, so **stay-tuned!**
---

### 🔗 Connect

I’m building Prevalis Strategies as a technical + strategic consulting venture. Follow the journey, learn with me, or drop suggestions or questions!

> **Domain:** [https://prevalis.ai](https://prevalis.ai)  
> **Email:** [info@prevalis.ai]  
> **Built & maintained by:** prevalis.ai ✨