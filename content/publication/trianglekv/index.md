---
title: 'TriangleKV: Reducing Write Stalls and Write Amplification in LSM-tree Based KV Stores with Triangle Container in NVM'

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - admin
  - Ting Yao
  - Hong Jiang
  - Qiu Cui
  - Liu Tang
  - Yiwen Zhang
  - Jiguang Wan
  - Zhihu Tan

# Author notes (optional)
# author_notes:
#   - 'Equal contribution'
#   - 'Equal contribution'
#   - 'Equal contribution'

date: '2022-07-04T00:00:00Z'
doi: ''

# Schedule page publish date (NOT publication's date).
publishDate: '2017-01-01T00:00:00Z'

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ['2']

# Publication name and optional abbreviated publication name.
publication: In *IEEE Transactions on Parallel and Distributed Systems*
publication_short: "TPDS"

abstract: Popular LSM-tree based key-value stores suffer from suboptimal and unpredictable performance due to write amplification and write stalls that cause application performance to periodically drop to nearly zero. Our preliminary experimental studies reveal that (1) write stalls mainly stem from the significantly large amount of data involved in each compaction between L0-L1 (i.e., the first two levels of LSM-tree), and (2) write amplification increases with the depth of LSM-trees. Existing work mainly focus on reducing write amplification, while only a couple of them target mitigating write stalls. In this paper, we exploit unique features of non-volatile memory (NVM) to address these two limitations and propose TriangleKV, a new LSM-tree based persistent KV store with multi-tier DRAM-NVM-SSD storage. TriangleKV’s design principles include performing smaller and cheaper L0-L1 compaction to reduce write stalls while reducing the depth of LSM-trees to mitigate write amplification. To this end, four novel techniques are proposed. First, we relocate and manage the L0 level in NVM with our proposed triangle container. Second, the new right-angle side compaction is devised to compact L0 to L1 at fine-grained key ranges, thus substantially reducing the amount of compaction data. Third, TriangleKV increases the width of each level to decrease the depth of LSM-trees thus mitigating write amplification. Finally, the cross-row hint search is introduced for the triangle container to keep adequate read performance. We implement TriangleKV based on MatrixKV and evaluate it on a hybrid DRAM/NVM/SSD system using Intel’s latest 3D Xpoint NVM device Optane DC PMM. Evaluation results show that, with the same amount of NVM, TriangleKV outperforms RocksDB, NoveLSM and MatrixKV in 99th-percentile latencies by 5.5×, 2.1× and 1.1×, and random write throughput by 4.9×, 3.5× and 1.4× respectively.

# Summary. An optional shortened abstract.
summary: ""

tags: [Key-Value Store, LSM-tree, Persistent Memory]

# Display this page in the Featured widget?
featured: false

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_pdf: 'https://ieeexplore.ieee.org/document/9815150'
url_code: 'https://github.com/CheneyDing/rocksdb/tree/trianglekv'
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
