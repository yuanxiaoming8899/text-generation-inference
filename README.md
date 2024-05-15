<div class="Box-sc-g0xbh4-0 bJMeLZ js-snippet-clipboard-copy-unpositioned" data-hpc="true"><article class="markdown-body entry-content container-lg" itemprop="text"><div align="center" dir="auto">
<a href="https://www.youtube.com/watch?v=jlMAX2Oaht0" rel="nofollow">
  <img width="560" alt="优化 TGI 部署" src="https://camo.githubusercontent.com/a4473598096b3cbdd8b9d3d189da29962a5d08502b17aa32ea3604bce36bc5ae/68747470733a2f2f68756767696e67666163652e636f2f64617461736574732f4e617273696c2f7467695f6173736574732f7265736f6c76652f6d61696e2f7468756d626e61696c2e706e67" data-canonical-src="https://huggingface.co/datasets/Narsil/tgi_assets/resolve/main/thumbnail.png" style="max-width: 100%;">
</a>
<div class="markdown-heading" dir="auto"><h1 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">文本生成推理</font></font></h1><a id="user-content-text-generation-inference" class="anchor" aria-label="永久链接：文本生成推理" href="#text-generation-inference"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<a href="https://github.com/huggingface/text-generation-inference">
  <img alt="GitHub 存储库星星" src="https://camo.githubusercontent.com/7d664bf1993aabe6d504a56b7532c6bbe54980c55fa95780f56f045d764c76e8/68747470733a2f2f696d672e736869656c64732e696f2f6769746875622f73746172732f68756767696e67666163652f746578742d67656e65726174696f6e2d696e666572656e63653f7374796c653d736f6369616c" data-canonical-src="https://img.shields.io/github/stars/huggingface/text-generation-inference?style=social" style="max-width: 100%;">
</a>
<a href="https://huggingface.github.io/text-generation-inference" rel="nofollow">
  <img alt="Swagger API 文档" src="https://camo.githubusercontent.com/f75caf3d4d8c8f4f15d6c994c2102a9baddd4cf81f37f09528e28122813472af/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f4150492d537761676765722d696e666f726d6174696f6e616c" data-canonical-src="https://img.shields.io/badge/API-Swagger-informational" style="max-width: 100%;">
</a>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">用于文本生成推理的 Rust、Python 和 gRPC 服务器。在</font></font><a href="https://huggingface.co" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">HuggingFace</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">的生产中用于
为 Hugging Chat、推理 API 和推理端点提供支持。</font></font></p>
</div>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">目录</font></font></h2><a id="user-content-table-of-contents" class="anchor" aria-label="永久链接：目录" href="#table-of-contents"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<ul dir="auto">
<li><a href="#get-started"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">开始使用</font></font></a>
<ul dir="auto">
<li><a href="#api-documentation"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">API文档</font></font></a></li>
<li><a href="#using-a-private-or-gated-model"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">使用私有或门控模型</font></font></a></li>
<li><a href="#a-note-on-shared-memory-shm"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">关于共享内存的注释</font></font></a></li>
<li><a href="#distributed-tracing"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">分布式追踪</font></font></a></li>
<li><a href="#local-install"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">本地安装</font></font></a></li>
<li><a href="#cuda-kernels"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">CUDA 内核</font></font></a></li>
</ul>
</li>
<li><a href="#optimized-architectures"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">优化架构</font></font></a></li>
<li><a href="#run-a-model"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">运行米斯特拉尔</font></font></a>
<ul dir="auto">
<li><a href="#run"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">跑步</font></font></a></li>
<li><a href="#quantization"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">量化</font></font></a></li>
</ul>
</li>
<li><a href="#develop"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">发展</font></font></a></li>
<li><a href="#testing"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">测试</font></font></a></li>
</ul>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">文本生成推理 (TGI) 是一个用于部署和服务大型语言模型 (LLM) 的工具包。 TGI 为最流行的开源 LLM 提供高性能文本生成，包括 Llama、Falcon、StarCoder、BLOOM、GPT-NeoX</font></font><a href="https://huggingface.co/docs/text-generation-inference/supported_models" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">等</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。 TGI 实现了许多功能，例如：</font></font></p>
<ul dir="auto">
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">简单的启动器，可为最受欢迎的法学硕士提供服务</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">生产就绪（使用开放遥测、Prometheus 指标进行分布式跟踪）</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">张量并行可在多个 GPU 上实现更快的推理</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">使用服务器发送事件 (SSE) 的令牌流</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">连续批处理传入请求以提高总吞吐量</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">在最流行的架构上使用</font></font><a href="https://github.com/HazyResearch/flash-attention"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Flash Attention</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">和</font></font><a href="https://github.com/vllm-project/vllm"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Paged Attention</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">进行推理的优化转换器代码</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">量化：
</font></font><ul dir="auto">
<li><a href="https://github.com/TimDettmers/bitsandbytes"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">位和字节</font></font></a></li>
<li><a href="https://arxiv.org/abs/2210.17323" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">GPT-Q</font></font></a></li>
<li><a href="https://github.com/NetEase-FuXi/EETQ"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">EETQ</font></font></a></li>
<li><a href="https://github.com/casper-hansen/AutoAWQ"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">加权平均质量</font></font></a></li>
</ul>
</li>
<li><a href="https://github.com/huggingface/safetensors"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Safetensors</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">重量加载</font></font></li>
<li><font style="vertical-align: inherit;"><a href="https://arxiv.org/abs/2301.10226" rel="nofollow"><font style="vertical-align: inherit;">使用大型语言模型的水印</font></a><font style="vertical-align: inherit;">进行水印</font></font><a href="https://arxiv.org/abs/2301.10226" rel="nofollow"><font style="vertical-align: inherit;"></font></a></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Logits 扭曲器（温度缩放、top-p、top-k、重复惩罚，更多详细信息请参见</font></font><a href="https://huggingface.co/docs/transformers/internal/generation_utils#transformers.LogitsProcessor" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Transformers.LogitsProcessor</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">）</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">停止序列</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">对数概率</font></font></li>
<li><a href="https://huggingface.co/docs/text-generation-inference/conceptual/speculation" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">猜测</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">~2 倍延迟</font></font></li>
<li><a href="https://huggingface.co/docs/text-generation-inference/conceptual/guidance" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">指南/JSON</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。指定输出格式以加速推理并确保输出根据某些规范有效。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">自定义提示生成：通过提供自定义提示来指导模型的输出，轻松生成文本</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">微调支持：利用针对特定任务的微调模型来实现更高的准确性和性能</font></font></li>
</ul>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">硬件支持</font></font></h3><a id="user-content-hardware-support" class="anchor" aria-label="永久链接：硬件支持" href="#hardware-support"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<ul dir="auto">
<li><a href="https://github.com/huggingface/text-generation-inference/pkgs/container/text-generation-inference"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">英伟达</font></font></a></li>
<li><a href="https://github.com/huggingface/text-generation-inference/pkgs/container/text-generation-inference"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">AMD</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">（-rocm）</font></font></li>
<li><a href="https://github.com/huggingface/optimum-neuron/tree/main/text-generation-inference"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">推论</font></font></a></li>
<li><a href="https://github.com/huggingface/text-generation-inference/pull/1475" data-hovercard-type="pull_request" data-hovercard-url="/huggingface/text-generation-inference/pull/1475/hovercard"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">英特尔GPU</font></font></a></li>
<li><a href="https://github.com/huggingface/tgi-gaudi"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">高迪</font></font></a></li>
<li><a href="https://huggingface.co/docs/optimum-tpu/howto/serving" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">谷歌TPU</font></font></a></li>
</ul>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">开始使用</font></font></h2><a id="user-content-get-started" class="anchor" aria-label="永久链接：开始" href="#get-started"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">码头工人</font></font></h3><a id="user-content-docker" class="anchor" aria-label="永久链接：Docker" href="#docker"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">有关详细的入门指南，请参阅</font></font><a href="https://huggingface.co/docs/text-generation-inference/quicktour" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">快速浏览</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。最简单的入门方法是使用官方 Docker 容器：</font></font></p>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>model=HuggingFaceH4/zephyr-7b-beta
volume=<span class="pl-smi">$PWD</span>/data <span class="pl-c"><span class="pl-c">#</span> share a volume with the Docker container to avoid downloading weights every run</span>

docker run --gpus all --shm-size 1g -p 8080:80 -v <span class="pl-smi">$volume</span>:/data ghcr.io/huggingface/text-generation-inference:2.0 --model-id <span class="pl-smi">$model</span></pre><div class="zeroclipboard-container">
   
  
    </clipboard-copy>
  </div></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">然后你可以提出这样的请求</font></font></p>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>curl 127.0.0.1:8080/generate_stream \
    -X POST \
    -d <span class="pl-s"><span class="pl-pds">'</span>{"inputs":"What is Deep Learning?","parameters":{"max_new_tokens":20}}<span class="pl-pds">'</span></span> \
    -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span></pre><div class="zeroclipboard-container">
   
    
</svg>
    </clipboard-copy>
  </div></div>
<p dir="auto"><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">注意：</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">要使用 NVIDIA GPU，您需要安装</font></font><a href="https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/install-guide.html" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">NVIDIA Container Toolkit</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。我们还建议使用 CUDA 版本 12.2 或更高版本的 NVIDIA 驱动程序。对于在没有 GPU 或 CUDA 支持的计算机上运行 Docker 容器，删除该</font></font><code>--gpus all</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">标志并添加就足够了</font></font><code>--disable-custom-kernels</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">，请注意 CPU 不是该项目的预期平台，因此性能可能会低于标准。</font></font></p>
<p dir="auto"><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">注意：</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;"> TGI 支持 AMD Instinct MI210 和 MI250 GPU。详细信息可以在</font></font><a href="https://huggingface.co/docs/text-generation-inference/supported_models#supported-hardware" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持的硬件文档</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">中找到。要使用 AMD GPU，请使用</font></font><code>docker run --device /dev/kfd --device /dev/dri --shm-size 1g -p 8080:80 -v $volume:/data ghcr.io/huggingface/text-generation-inference:2.0-rocm --model-id $model</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">而不是上面的命令。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">要查看为模型提供服务的所有选项（在代码</font></font><a href="https://github.com/huggingface/text-generation-inference/blob/main/launcher/src/main.rs"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">或</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">cli 中）：</font></font></p>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>text-generation-launcher --help
</code></pre><div class="zeroclipboard-container">
   
    
     
</svg>
    </clipboard-copy>
  </div></div>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">API文档</font></font></h3><a id="user-content-api-documentation" class="anchor" aria-label="永久链接：API 文档" href="#api-documentation"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"></font><code>text-generation-inference</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">您可以使用该路由</font><font style="vertical-align: inherit;">查阅REST API的OpenAPI文档</font></font><code>/docs</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。 Swagger UI 也可从以下网址获取：</font></font><a href="https://huggingface.github.io/text-generation-inference" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">https://huggingface.github.io/text- Generation-inference</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></p>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">使用私有或门控模型</font></font></h3><a id="user-content-using-a-private-or-gated-model" class="anchor" aria-label="永久链接：使用私有或门控模型" href="#using-a-private-or-gated-model"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">您可以选择使用</font></font><code>HUGGING_FACE_HUB_TOKEN</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">环境变量来配置 所使用的令牌
</font></font><code>text-generation-inference</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。这允许您访问受保护的资源。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">例如，如果您想提供门控 Llama V2 模型变体：</font></font></p>
<ol dir="auto">
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">前往</font></font><a href="https://huggingface.co/settings/tokens" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">https://huggingface.co/settings/tokens</font></font></a></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">复制您的 cli READ 令牌</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">出口</font></font><code>HUGGING_FACE_HUB_TOKEN=&lt;your cli READ token&gt;</code></li>
</ol>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">或使用 Docker：</font></font></p>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>model=meta-llama/Llama-2-7b-chat-hf
volume=<span class="pl-smi">$PWD</span>/data <span class="pl-c"><span class="pl-c">#</span> share a volume with the Docker container to avoid downloading weights every run</span>
token=<span class="pl-k">&lt;</span>your cli READ token<span class="pl-k">&gt;</span>

docker run --gpus all --shm-size 1g -e HUGGING_FACE_HUB_TOKEN=<span class="pl-smi">$token</span> -p 8080:80 -v <span class="pl-smi">$volume</span>:/data ghcr.io/huggingface/text-generation-inference:2.0 --model-id <span class="pl-smi">$model</span></pre><div class="zeroclipboard-container">
   
     
</svg>
    </clipboard-copy>
  </div></div>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">关于共享内存 (shm) 的注释</font></font></h3><a id="user-content-a-note-on-shared-memory-shm" class="anchor" aria-label="永久链接：关于共享内存 (shm) 的说明" href="#a-note-on-shared-memory-shm"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><a href="https://docs.nvidia.com/deeplearning/nccl/user-guide/docs/index.html" rel="nofollow"><code>NCCL</code></a><font style="vertical-align: inherit;"></font><code>PyTorch</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">是用于进行分布式训练/推理的</font><font style="vertical-align: inherit;">通信框架
。</font></font><code>text-generation-inference</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">利用</font></font><code>NCCL</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">张量并行性来显着加快大型语言模型的推理速度。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">为了在</font></font><code>NCCL</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">组中的不同设备之间共享数据，</font></font><code>NCCL</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">如果无法使用 NVLink 或 PCI 进行点对点，则可能会转而使用主机内存。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">为了让容器使用1G的共享内存并支持SHM共享，我们添加</font></font><code>--shm-size 1g</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">上面的命令。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"></font><code>text-generation-inference</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">如果你在里面</font><font style="vertical-align: inherit;">跑</font></font><code>Kubernetes</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。您还可以通过使用以下命令创建卷来将共享内存添加到容器中：</font></font></p>
<div class="highlight highlight-source-yaml notranslate position-relative overflow-auto" dir="auto"><pre>- <span class="pl-ent">name</span>: <span class="pl-s">shm</span>
  <span class="pl-ent">emptyDir</span>:
   <span class="pl-ent">medium</span>: <span class="pl-s">Memory</span>
   <span class="pl-ent">sizeLimit</span>: <span class="pl-s">1Gi</span></pre><div class="zeroclipboard-container">
    
    
</svg>
    </clipboard-copy>
  </div></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">并将其安装到</font></font><code>/dev/shm</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">.</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">最后，您还可以使用环境变量禁用SHM共享</font></font><code>NCCL_SHM_DISABLE=1</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。但请注意，这会影响性能。</font></font></p>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">分布式追踪</font></font></h3><a id="user-content-distributed-tracing" class="anchor" aria-label="永久链接：分布式跟踪" href="#distributed-tracing"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><code>text-generation-inference</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">使用 OpenTelemetry 进行分布式跟踪。您可以通过使用参数设置 OTLP 收集器的地址来使用此功能</font></font><code>--otlp-endpoint</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></p>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">建筑学</font></font></h3><a id="user-content-architecture" class="anchor" aria-label="永久链接：建筑" href="#architecture"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><a target="_blank" rel="noopener noreferrer nofollow" href="https://camo.githubusercontent.com/ce740adb6387a12d2b15e570faa4c02177c99d4f059d12a1b9a44492640014dc/68747470733a2f2f68756767696e67666163652e636f2f64617461736574732f68756767696e67666163652f646f63756d656e746174696f6e2d696d616765732f7265736f6c76652f6d61696e2f5447492e706e67"><img src="https://camo.githubusercontent.com/ce740adb6387a12d2b15e570faa4c02177c99d4f059d12a1b9a44492640014dc/68747470733a2f2f68756767696e67666163652e636f2f64617461736574732f68756767696e67666163652f646f63756d656e746174696f6e2d696d616765732f7265736f6c76652f6d61696e2f5447492e706e67" alt="TGI架构" data-canonical-src="https://huggingface.co/datasets/huggingface/documentation-images/resolve/main/TGI.png" style="max-width: 100%;"></a></p>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">本地安装</font></font></h3><a id="user-content-local-install" class="anchor" aria-label="永久链接：本地安装" href="#local-install"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">您也可以选择本地安装</font></font><code>text-generation-inference</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">首先</font></font><a href="https://rustup.rs/" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">安装 Rust</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">并创建一个至少包含 Python 3.9 的 Python 虚拟环境，例如使用</font></font><code>conda</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">：</font></font></p>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>curl --proto <span class="pl-s"><span class="pl-pds">'</span>=https<span class="pl-pds">'</span></span> --tlsv1.2 -sSf https://sh.rustup.rs <span class="pl-k">|</span> sh

conda create -n text-generation-inference python=3.11
conda activate text-generation-inference</pre><div class="zeroclipboard-container">
    
    
    
</svg>
    </clipboard-copy>
  </div></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">您可能还需要安装 Protoc。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">在 Linux 上：</font></font></p>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>PROTOC_ZIP=protoc-21.12-linux-x86_64.zip
curl -OL https://github.com/protocolbuffers/protobuf/releases/download/v21.12/<span class="pl-smi">$PROTOC_ZIP</span>
sudo unzip -o <span class="pl-smi">$PROTOC_ZIP</span> -d /usr/local bin/protoc
sudo unzip -o <span class="pl-smi">$PROTOC_ZIP</span> -d /usr/local <span class="pl-s"><span class="pl-pds">'</span>include/*<span class="pl-pds">'</span></span>
rm -f <span class="pl-smi">$PROTOC_ZIP</span></pre><div class="zeroclipboard-container">
    
  
     
</svg>
    </clipboard-copy>
  </div></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">在 MacOS 上，使用 Homebrew：</font></font></p>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>brew install protobuf</pre><div class="zeroclipboard-container">
    
    
   
</svg>
    </clipboard-copy>
  </div></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">然后运行：</font></font></p>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>BUILD_EXTENSIONS=True make install <span class="pl-c"><span class="pl-c">#</span> Install repository and HF/transformer fork with CUDA kernels</span>
text-generation-launcher --model-id mistralai/Mistral-7B-Instruct-v0.2</pre><div class="zeroclipboard-container">
   
     
    
</svg>
    </clipboard-copy>
  </div></div>
<p dir="auto"><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">注意：</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">在某些计算机上，您可能还需要 OpenSSL 库和 gcc。在 Linux 机器上，运行：</font></font></p>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>sudo apt-get install libssl-dev gcc -y</pre><div class="zeroclipboard-container">
    
    
      
</svg>
    </clipboard-copy>
  </div></div>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">优化架构</font></font></h2><a id="user-content-optimized-architectures" class="anchor" aria-label="永久链接：优化的架构" href="#optimized-architectures"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">TGI 开箱即用，为所有现代模型提供优化模型。您可以在</font></font><a href="https://huggingface.co/docs/text-generation-inference/supported_models" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">此列表</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">中找到它们</font><font style="vertical-align: inherit;">。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">尽最大努力支持其他架构：</font></font></p>
<p dir="auto"><code>AutoModelForCausalLM.from_pretrained(&lt;model&gt;, device_map="auto")</code></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">或者</font></font></p>
<p dir="auto"><code>AutoModelForSeq2SeqLM.from_pretrained(&lt;model&gt;, device_map="auto")</code></p>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">本地运行</font></font></h2><a id="user-content-run-locally" class="anchor" aria-label="永久链接：本地运行" href="#run-locally"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">跑步</font></font></h3><a id="user-content-run" class="anchor" aria-label="永久链接： 运行" href="#run"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>text-generation-launcher --model-id mistralai/Mistral-7B-Instruct-v0.2</pre><div class="zeroclipboard-container">
   
    
     
  </div></div>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">量化</font></font></h3><a id="user-content-quantization" class="anchor" aria-label="永久链接：量化" href="#quantization"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">您还可以使用位和字节量化权重，以减少 VRAM 要求：</font></font></p>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>text-generation-launcher --model-id mistralai/Mistral-7B-Instruct-v0.2 --quantize</pre><div class="zeroclipboard-container">
   
   
      
  </div></div>
<p dir="auto"><font style="vertical-align: inherit;"></font><a href="https://arxiv.org/pdf/2305.14314.pdf" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">使用bitsandbytes 中的 NF4 和 FP4 数据类型</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">可以进行 4 位量化</font><font style="vertical-align: inherit;">。可以通过提供</font></font><code>--quantize bitsandbytes-nf4</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">或</font></font><code>--quantize bitsandbytes-fp4</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">作为命令行参数来启用它</font></font><code>text-generation-launcher</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></p>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">发展</font></font></h2><a id="user-content-develop" class="anchor" aria-label="永久链接： 开发" href="#develop"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>make server-dev
make router-dev</pre><div class="zeroclipboard-container">
   
    
     
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">测试</font></font></h2><a id="user-content-testing" class="anchor" aria-label="永久链接：测试" href="#testing"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-c"><span class="pl-c">#</span> python</span>
make python-server-tests
make python-client-tests
<span class="pl-c"><span class="pl-c">#</span> or both server and client tests</span>
make python-tests
<span class="pl-c"><span class="pl-c">#</span> rust cargo tests</span>
make rust-tests
<span class="pl-c"><span class="pl-c">#</span> integration tests</span>
make integration-tests</pre><div class="zeroclipboard-container">
   
     
     
    </clipboard-copy>
  </div></div>
</article></div>
