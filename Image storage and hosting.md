# Image storage and hosting

What hosted services are there for hosting and serving images (and potentially other assets like videos or pdfs).

Bonus if good management options -- this makes it more like "digital asset managment"

## Options

- Cloudinary
- Bytescale
- Raw cloud storage like S3 or R2
- R2 with its image functionality

## Bytescale looks like a great semi-open-source option with backing onto r2 (from $35/month)

> From https://github.com/orgs/life-itself/discussions/436#discussioncomment-7141697 (Sep 2023)

Just came across Bytescale: https://www.bytescale.com/pricing (formely upload.io)

Present as a developer oriented cloundinary alternative.

More relevantly for us they are a frontend and processing pipeline for r2 (or s3 etc) which gives us a combination of UX and portability (from our own storage).

![image](https://github.com/life-itself/community/assets/180658/15676968-68c1-4531-96ab-bdc430b25e7a)

Notes

- Added R2 support July 2023 https://www.bytescale.com/blog/cloudflare-r2-support-released/
- Need the $35/month plan (vs $7 basic) to support r2 and to have up to 5 team members (vs 1 on the basic plan)

### Good, fast, simple upload experience

here's the result

![image](https://github.com/life-itself/community/assets/180658/cd1e3dd7-2104-4bf5-8a7e-4f5f3c2c2575)

# Related

Relates to DAMs and digital asset management

# Inbox

https://github.com/orgs/life-itself/discussions/436
