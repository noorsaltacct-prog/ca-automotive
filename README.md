# CA Automotive — Website Preview

A fast, static website built for Charlie at CA Automotive in Columbus, Ohio.

## Publish without a command line

1. Unzip the download. Open the unzipped folder and select **everything inside** (index.html, assets, gallery, and the other files).
2. On GitHub, create a new repository. Select **Add file > Upload files**, drag in all the unzipped contents, and commit the upload. Preserve the folder structure.
3. On Vercel, choose **Add New > Project**, import the GitHub repository, set **Framework Preset** to **Other**, and choose **Deploy**. No build command is required.
4. The eight work photos are already included in **gallery/photo-1.jpg** through **gallery/photo-8.jpg**. To change them, upload replacement photos with those same names into the gallery folder on GitHub. The site gallery automatically uses those files. To add/remove slots, edit the **GALLERY_IMAGES** array at the top of **assets/js/main.js**.
5. The phone number is currently **614-902-7078**. To change it, update the telephone links in **index.html** and the **PHONE** value near the top of **assets/js/main.js**. When Charlie provides an email address, set **CONTACT_EMAIL** in main.js. For online form delivery, paste a Formspree-style endpoint into **FORM_ENDPOINT** in main.js. Until configured, submitting the form opens a prepared text message to Charlie; the visitor must tap Send. Verify the form after deployment.
6. To connect a domain, add it in the Vercel project's **Domains** settings and follow the displayed DNS instructions. Then replace **[YOUR-DOMAIN]** in **index.html** (canonical link, Open Graph URL, and JSON-LD), **sitemap.xml**, and **robots.txt** with the real domain. Do not include brackets in the finished domain.

## Before launch

- Confirm operating hours, availability, service radius, and the exact scope of services with Charlie.
- The logo is stored in **assets/logo.webp** and a simplified red CA emblem is in **assets/favicon.svg**.
- The hero uses Charlie's actual engine-work photo. No stock or AI-generated images are used.
- Customer reviews were intentionally not invented. Add real, permissioned testimonials if available.
- Confirm the business wants to accept requests through the displayed number and test the call, text, and form buttons on a phone.
- If gallery photos are replaced under the same filenames after launch, browsers may retain cached copies. Rename the photo files and update the gallery array or redeploy with a cache-busting filename when necessary.
