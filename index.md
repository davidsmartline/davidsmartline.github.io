---
layout: page
title: "Home"
date: 2026-07-06
---

Hello, this is Smart Line's open ideas!

<!doctype html>
<html lang="zh-CN">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <meta name="description" content="Paper website: title, abstract, links to PDF/code/data." />
  <title>论文标题｜Paper Website</title>

  <style>
    :root{
      --bg:#0b1020; --card:#111a33; --text:#e9eefc; --muted:#a9b3d6;
      --line:rgba(255,255,255,.12); --accent:#7aa2ff; --accent2:#7cffc4;
      --shadow: 0 10px 30px rgba(0,0,0,.35);
      --radius: 18px;
      --max: 1060px;
    }
    *{box-sizing:border-box}
    html,body{margin:0;padding:0;font-family: ui-sans-serif,system-ui,-apple-system,Segoe UI,Roboto,Helvetica,Arial,"PingFang SC","Noto Sans CJK SC","Microsoft YaHei",sans-serif;background:radial-gradient(1200px 800px at 10% 0%, rgba(122,162,255,.22), transparent 60%),radial-gradient(900px 600px at 90% 10%, rgba(124,255,196,.14), transparent 55%), var(--bg);color:var(--text)}
    a{color:var(--accent);text-decoration:none}
    a:hover{text-decoration:underline}
    .wrap{max-width:var(--max);margin:0 auto;padding:28px 18px 60px}
    .topbar{display:flex;align-items:center;justify-content:space-between;gap:14px;position:sticky;top:0;background:rgba(11,16,32,.72);backdrop-filter: blur(10px);border-bottom:1px solid var(--line);padding:14px 18px;margin:0 -18px 18px;z-index:10}
    .brand{display:flex;align-items:center;gap:10px}
    .dot{width:10px;height:10px;border-radius:999px;background:linear-gradient(135deg,var(--accent),var(--accent2));box-shadow:0 0 18px rgba(122,162,255,.45)}
    .nav{display:flex;flex-wrap:wrap;gap:10px}
    .nav a{font-size:14px;color:var(--muted);padding:8px 10px;border:1px solid transparent;border-radius:999px}
    .nav a:hover{border-color:var(--line);color:var(--text);text-decoration:none}

    .hero{display:grid;grid-template-columns: 1.15fr .85fr;gap:18px;align-items:stretch}
    @media (max-width: 900px){.hero{grid-template-columns:1fr}}
    .card{background:linear-gradient(180deg, rgba(255,255,255,.04), rgba(255,255,255,.02));border:1px solid var(--line);border-radius:var(--radius);box-shadow:var(--shadow)}
    .heroL{padding:22px}
    .title{font-size:34px;line-height:1.15;margin:0 0 8px}
    .subtitle{margin:0 0 14px;color:var(--muted);font-size:15px}
    .authors{margin:0 0 16px;color:var(--text);font-size:15px}
    .authors span{color:var(--muted)}
    .badges{display:flex;flex-wrap:wrap;gap:10px;margin:14px 0 6px}
    .btn{display:inline-flex;align-items:center;gap:8px;padding:10px 12px;border-radius:12px;border:1px solid var(--line);background:rgba(255,255,255,.03);color:var(--text);font-size:14px}
    .btn:hover{transform: translateY(-1px);transition:120ms; text-decoration:none;border-color: rgba(122,162,255,.35)}
    .btn strong{font-weight:600}
    .note{margin:10px 0 0;color:var(--muted);font-size:13px}

    .heroR{padding:14px;display:flex;flex-direction:column;gap:12px}
    .teaser{border-radius:14px;border:1px solid var(--line);overflow:hidden;background:rgba(255,255,255,.02)}
    .teaser img{display:block;width:100%;height:auto}
    .teaser .cap{padding:10px 12px;color:var(--muted);font-size:13px;border-top:1px solid var(--line)}

    .grid{display:grid;grid-template-columns: 1fr 1fr;gap:18px;margin-top:18px}
    @media (max-width: 900px){.grid{grid-template-columns:1fr}}
    section.card{padding:18px}
    h2{margin:0 0 10px;font-size:20px}
    p{margin:10px 0;color:var(--text);line-height:1.7}
    ul{margin:10px 0 0 20px;color:var(--text);line-height:1.7}
    code.inline{background:rgba(255,255,255,.06);border:1px solid var(--line);padding:2px 6px;border-radius:8px;color:var(--text)}
    pre{margin:12px 0;background:rgba(0,0,0,.35);border:1px solid var(--line);border-radius:14px;padding:12px;overflow:auto}
    pre code{color:#d9e2ff;font-family: ui-monospace,SFMono-Regular,Menlo,Monaco,Consolas,"Liberation Mono","Courier New",monospace;font-size:13px}
    .kv{display:grid;grid-template-columns: 130px 1fr;gap:10px;border-top:1px dashed var(--line);padding-top:12px;margin-top:12px}
    .kv div{color:var(--muted);font-size:14px}
    .kv b{color:var(--text);font-weight:600}
    .foot{margin-top:18px;color:var(--muted);font-size:13px;text-align:center}
    .hr{height:1px;background:var(--line);margin:18px 0}
  </style>
</head>

<body>
  <div class="wrap">
    <div class="topbar">
      <div class="brand">
        <div class="dot"></div>
        <div>
          <div style="font-weight:700;letter-spacing:.2px">Paper Website</div>
          <div style="font-size:12px;color:var(--muted)">GitHub Pages · 单页论文站</div>
        </div>
      </div>
      <div class="nav">
        <a href="#abstract">摘要</a>
        <a href="#method">方法</a>
        <a href="#results">结果</a>
        <a href="#video">演示</a>
        <a href="#download">下载</a>
        <a href="#citation">引用</a>
      </div>
    </div>

    <div class="hero">
      <div class="card heroL">
        <h1 class="title">这里填论文标题：A Practical XYZ for …</h1>
        <p class="subtitle">会议/期刊/技术报告信息（可选）：Submitted to XXX · 2026</p>

        <p class="authors">
          <b>Author A</b><sup>1</sup>, <b>Author B</b><sup>1</sup>, <b>Author C</b><sup>2</sup>
          <br/>
          <span><sup>1</sup>机构/公司名 · <sup>2</sup>合作单位</span>
        </p>

        <div class="badges" id="download">
          <a class="btn" href="./paper.pdf" target="_blank" rel="noopener">
            📄 <strong>PDF</strong>
          </a>
          <a class="btn" href="https://github.com/你的用户名/你的仓库" target="_blank" rel="noopener">
            💻 <strong>Code</strong>
          </a>
          <a class="btn" href="https://github.com/你的用户名/你的仓库/releases" target="_blank" rel="noopener">
            📦 <strong>Release</strong>
          </a>
          <a class="btn" href="mailto:your_email@example.com">
            ✉️ <strong>Contact</strong>
          </a>
        </div>

        <p class="note">
          建议把 <code class="inline">paper.pdf</code> 放在仓库根目录。图放在 <code class="inline">assets/</code>。
        </p>

        <div class="kv">
          <div>关键词</div><div><b>robotics</b>, long-reach arm, force control, grinding</div>
          <div>版本</div><div><b>v1.0</b> (2026-02-23)</div>
        </div>
      </div>

      <div class="card heroR">
        <div class="teaser">
          <!-- 可选：放一张“teaser”图 -->
          <img src="./assets/teaser.png" alt="Teaser figure (optional)" onerror="this.style.display='none'">
          <div class="cap">图 1：Teaser（可选）。如果没放图片，此处会自动隐藏。</div>
        </div>

        <div class="card" style="padding:14px">
          <h2 style="margin:0 0 8px;font-size:16px">亮点（可改成 3–5 条）</h2>
          <ul style="margin-top:6px">
            <li>提出一种可落地的 XYZ 方法，减少人工调参。</li>
            <li>在真实工业任务上验证（如磨削/焊接/装配）。</li>
            <li>开源：代码 + 数据 + 复现实验脚本。</li>
          </ul>
        </div>
      </div>
    </div>

    <div class="grid">
      <section class="card" id="abstract">
        <h2>摘要</h2>
        <p>
          在这里写一段摘要：说明问题、方法、结果和贡献。建议 120–200 字（或英文 120–200 words）。
          如果你要中英双语，也可以在下面再加一段英文。
        </p>
        <div class="hr"></div>
        <p style="color:var(--muted)">
          Abstract (EN): Optional English abstract here…
        </p>
      </section>

      <section class="card" id="method">
        <h2>方法概述</h2>
        <p>
          用 2–4 段介绍方法，配合 1–2 张关键图（可以放在 assets/ 里，然后用 &lt;img&gt; 插入）。
        </p>
        <ul>
          <li>系统结构：传感器 → 决策 → 执行</li>
          <li>关键算法：例如力控、视觉定位、轨迹规划</li>
          <li>工程实现：实时性、鲁棒性、安全策略</li>
        </ul>
      </section>

      <section class="card" id="results">
        <h2>实验与结果</h2>
        <p>
          展示主要指标：精度、效率、成功率、磨削表面粗糙度、能耗等。建议放对比表或曲线图。
        </p>
        <pre><code>// 示例：把复现实验写得很明确
# install
pip install -r requirements.txt

# run demo
python demo.py --config configs/default.yaml
</code></pre>
      </section>

      <section class="card" id="video">
        <h2>演示视频</h2>
        <p>如果你有 YouTube/Bilibili 视频，可用 iframe 嵌入（注意部分地区网络限制）。</p>

        <!-- 例：YouTube -->
        <!--
        <div style="border:1px solid var(--line);border-radius:14px;overflow:hidden">
          <iframe width="100%" height="315" src="https://www.youtube.com/embed/VIDEO_ID"
            title="demo video" frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen></iframe>
        </div>
        -->

        <p style="color:var(--muted)">也可以只放链接：<a href="#">Demo Video Link</a></p>
      </section>

      <section class="card" id="citation" style="grid-column: 1 / -1;">
        <h2>引用（BibTeX）</h2>
        <p>把下面内容改成你的论文信息（title/authors/year/venue/doi/url）。</p>
        <pre><code>@article{yourkey2026xyz,
  title   = {Your Paper Title},
  author  = {Author A and Author B and Author C},
  journal = {arXiv preprint arXiv:xxxx.xxxxx},
  year    = {2026},
  url     = {https://yourusername.github.io/yourrepo/}
}</code></pre>

        <div class="hr"></div>
        <h2>许可与声明</h2>
        <p style="color:var(--muted)">
          建议明确：代码 License（MIT/Apache-2.0），论文版权归属，数据使用条款，以及与公司/合作单位的声明。
        </p>
      </section>
    </div>

    <div class="foot">
      © 2026 Your Name · Built with GitHub Pages
    </div>
  </div>
</body>
</html>
