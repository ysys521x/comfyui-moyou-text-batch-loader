comfyui-moyou-text-batch-loader 节点包

1. 安装方法：
   - 将comfyui-moyou-text-batch-loader文件夹复制到ComfyUI的custom_nodes目录
   - 无需额外依赖
   - 重启ComfyUI

2. 功能特点：
   - 与WAS Load Image Batch节点操作模式完全一致
   - 三种加载模式：single_text、incremental_text、random
   - 固定seed时random模式生成可复现的顺序
   - 严格分离的输出：
     - text_content：仅文本内容
     - filename：仅文件名
     - current_index：当前索引
     - total_count：总文件数

3. 使用方法：
   - 在「WAS Suite/IO」分类下找到「Moyou Text Batch Loader」节点
   - incremental_text模式下，每次运行自动加载下一个文本
   - 可分别连接文本内容和文件名到后续节点

4. 注意事项：
   - 确保path参数为文本文件所在目录的正确路径
   - 中文文本建议使用gbk编码
   - 更换目录后会自动重置加载状态
    