# 解析用 PDF 副本

该副本修正原 PDF 的裁剪框及书名页旋转，恢复被裁剪隐藏的内容；未重采样页面图像。原始 PDF 字节另存于 `../source/`。页面索引与原件相同，变更见本书 `processing_map.json`。本书结构化坐标对应此副本。

若存在分片，运行 `python3 reassemble.py` 恢复副本并校验 SHA-256。
