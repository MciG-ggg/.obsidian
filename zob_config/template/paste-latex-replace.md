---
words:
  2025-04-13: 110
---
<%*
    // 获取剪贴板内容而不是整个文件内容
    const clipboardContent = await navigator.clipboard.readText()
    if (clipboardContent) {
        // 处理\(公式\)格式
        let replacedContent = clipboardContent.replace(/\\\((.*?)\\\)/g, (_, p1) => '$' + p1.trim() + '$')
        
        // 处理\[公式\]格式 - 使用s标志使.能匹配换行符
        replacedContent = replacedContent.replace(/\\\[([\s\S]*?)\\\]/g, (_, p1) => '$$' + p1.trim() + '$$')
        
        // 返回处理后的内容
        tR = replacedContent
    } else {
        // 如果剪贴板为空，则不做任何处理
        tR = ""
    }
%>