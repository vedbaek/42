
# sphinx-quickstart

## 快速开始
### 新sphinx项目
```
sphinx-quickstart
```

### 生成html预览
```
make html
```

## 本地web服务
```
# 安装
pip install sphinx-autobuild

# 启动服务
sphinx-autobuild source build/html
```

## furo theme
```
pip install furo
```

## 依赖安装
```bash
python -m pip install -r requirements.txt
```

### requirements.txt
```
sphinx
sphinx-copybutton
sphinx_design
sphinx_inline_tabs
myst_parser
furo
```

## github Action
```
name: Deploy to Github Pages

on: [push, pull_request, workflow_dispatch]

permissions:
  contents: write

jobs:
  deploy-to-pages:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: actions/setup-python@v3
      - name: Install dependencies
        run: |
          python -m pip install --upgrade pip
          python -m pip install -r requirements.txt
      - name: Sphinx build
        run: |
          make html
      - name: Deploy to GitHub Pages
        uses: peaceiris/actions-gh-pages@v3
        if: ${{ github.event_name == 'push' && github.ref == 'refs/heads/main' }}
        with:
          publish_branch: gh-pages
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: build/html/
          force_orphan: true

```

## 参考
[1] Sphinx+gitee+Read the Docs搭建在线文档系统 https://zhuanlan.zhihu.com/p/384863296

[2] furo theme https://sphinx-themes.org/sample-sites/furo/

[3] markdown math https://myst-parser.readthedocs.io/en/latest/syntax/math.html

[4] math syntax https://myst-parser.readthedocs.io/en/v0.13.7/using/syntax.html#syntax-math

[5] LaTeX公式编辑器 https://www.latexlive.com/