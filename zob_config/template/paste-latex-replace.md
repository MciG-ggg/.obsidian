---
words:
  2025-04-13: 110
  2025-04-30: 62
---
<%*
    const clipboardContent = await navigator.clipboard.readText ();
    if (clipboardContent) {
        // 处理 $...$ 格式并去除两端空格
        le replacedContent = replacedContent.replace (/\$([\s\S]*?)\$/g, (_, p1) => '$' + p1.trim () + '$');
        
        tR = replacedContent;
    } else {
        tR = "";
    }
%>