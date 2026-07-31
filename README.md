# 生化专利代理人助手

基于 Streamlit 的中国发明专利撰写辅助工具：上传 `.docx`、`.txt`、`.md` 等技术材料，调用用户提供的 OpenAI 兼容 API 生成 Markdown 或 DOCX 草稿。生成内容包含单独的“原理说明”章节。

## 本地运行

```bash
python -m venv .venv
# Windows PowerShell
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt
streamlit run app.py
```

## 部署到 Streamlit Community Cloud

1. 将本项目推送到 GitHub 仓库。
2. 打开 <https://share.streamlit.io/> 并使用 GitHub 登录。
3. 选择仓库、分支和 `app.py`。
4. 点击 **Deploy**。
5. 在应用页面的侧边栏输入自己的 API Key、Base URL 和模型名称。

本应用不会将 API Key 写入代码或文件；不要把 API Key 提交到 GitHub。

## 支持的接口

默认使用 OpenAI API，也支持实现 Chat Completions 兼容接口的服务。用户可在页面侧边栏设置 Base URL 和模型名称。

## 重要提示

模型输出仅为专利撰写辅助草稿，不构成法律意见，也不能替代专利代理师审核、技术人员核验或真实实验数据。不得将模型生成的虚构数据作为实验结果使用。
