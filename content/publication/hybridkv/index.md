---
title: 'HybridKV: An Efficient Key-Value Store with HybridTree Index Structure Based on Non-Volatile Memory'

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - admin
  - Jiguang Wan
  - Rui Yan

# Author notes (optional)
# author_notes:
#   - 'Equal contribution'
#   - 'Equal contribution'
#   - 'Equal contribution'

date: '2021-03-01T00:00:00Z'
doi: ''

# Schedule page publish date (NOT publication's date).
publishDate: '2017-01-01T00:00:00Z'

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ['1']

# Publication name and optional abbreviated publication name.
publication: In *International Conference on Artificial Intelligence and Computer Science*
publication_short: "AICS"

abstract: Non-Volatile Memory (NVM) is a new type of storage media with non-volatile data, higher storage density, better performance and concurrency. Persistent key-value stores designed for earlier storage devices, using Log-Structured Merge Tree (LSM-Tree), have serious read-write amplification problem and do not take full advantage of these new devices. Existing works on NVM index structure are mostly based on Radix-Tree or B+-Tree, index structure based on Radix-Tree has better performance but takes up more space. In this paper, we present a new index structure named HybridTree on NVM. HybridTree combines the characteristics of Radix-Tree and B+-Tree. The upper layer is composed of prefix index nodes similar to Radix-Tree, which is indexed by the key prefix speed up data locating, and providing multi-thread support. The lower layer consists of variable-length adaptive B+-Tree nodes organizing key-value data to reduce space waste caused by node sparseness. We evaluate HybridTree on a real NVM devices (Inter Optane DC Persistent Memory). Evaluation results show that HybridTree’s random write performance is 1.2x to 1.62x compared to Fast & Fair and 1.11x to 1.52x compared to NV-Tree, with 54% space utilization reduced compared to WORT. We further integrate HybridTree into LevelDB to build a high performance key-value store HybridKV. By storing HybridTree directly on NVM, the problem of read and write amplification of LSM-Tree is avoided. We evaluate HybridKV on a hybrid DRAM/NVM systems, according to the results, HybridKV can improve random write performance by 7.5x compared to LevelDB and 3.23x compared to RocksDB. In addition, the random read performance of HybridKV is 7x compared to NoveLSM.

# Summary. An optional shortened abstract.
summary: ""

tags: [Key-Value Store, Persistent Memory, Index]

# Display this page in the Featured widget?
featured: false

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_pdf: 'https://iopscience.iop.org/article/10.1088/1742-6596/2025/1/012093/pdf'
url_code: ''
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# image:
#   caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/pLCdAaMFLTE)'
#   focal_point: ''
#   preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects: []

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---
