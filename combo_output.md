<think>
Okay, let's tackle this problem step by step. The user wants me to process a Markdown document and identify non-English phrases, then add their English translations in parentheses. But I need to make sure that existing English text remains unchanged. 

First, I'll look at the structure of the input. It's a table with columns like "全宗号", "全宗名称", etc. The first thing I notice is that the headers are in Chinese. For example, "全宗号" translates to "Collection Number". I need to check each cell in the table.

Looking at the first row of data: "XW024" is an identifier, probably not needing translation. Then "北京市宣武区饮食公司★" – this is a Chinese name. The "★" might be a symbol, but the main part is Chinese. So I should translate that to "Beijing Xuanwu District Catering Company" and add the parentheses.

Next, "1956~1999" – numbers and a tilde. Since numbers are universal, I don't need to translate that. Then "2331卷" – "卷" is Chinese for "volumes", so "2331 volumes".

I need to go through each cell. For example, "北京市宣武区土产杂品公司★" becomes "Beijing Xuanwu District Local Products Company". The "★" might indicate something, but the user didn't mention handling symbols, so just leave it as is.

I have to make sure that any English text like "Collection Number" remains unchanged. But in this case, the headers are all in Chinese. The entries like "北京市宣武区教育局" should be translated to "Beijing Xuanwu District Education Bureau".

Wait, the user mentioned that if the input has existing English, like "File Start and End Time", it should stay. But in this case, all the entries are in Chinese except for the identifiers like XW024, which are codes. So I don't need to worry about English text in the data cells.

Another thing: the example given had "2331卷" translated to "2331 volumes". So numbers with Chinese characters should be translated. So "卷" becomes "volumes", "件" becomes "items" or "pieces". But the user's example used "volumes" for "卷" and "件" was in the input as "2331卷 2643件" which would become "2331 volumes 2643 items".

I need to check each entry. For example, "北京市宣武区广安门外街道" translates to "Beijing Xuanwu District Guang'anmen Subdistrict". "街道" is "subdistrict".

Also, some entries have "★" – maybe indicating a specific note, but since the user didn't ask to translate symbols, just leave them.

Now, the headers: "全宗号" becomes "Collection Number", "全宗名称" becomes "Collection Name", "案卷起止时间" becomes "Case File Start and End Time", "案卷数量（卷、件）" becomes "Case File Quantity (Volumes, Items)".

Wait, the user's example for "全宗号" was translated as "Collection Number", so I should follow that. So the headers need to be translated as well. But the user's instruction says to process the entire document, including the headers.

So the first line is the header, which is all Chinese. Each header cell needs translation. Then the data rows, each cell that's non-English (which are all the entries except the identifiers like XW024) need translation.

So the final output should have the headers translated, and each data cell that's Chinese translated. The identifiers like XW024 remain as they are. The years and numbers with Chinese characters (like 2331卷) get translated.

I need to make sure that the Markdown structure is preserved. So the table remains the same, but with translations added where necessary.

Let me check the example given. The user's example had "全宗号" becoming "全宗号 (Collection Number)". So the same applies here. So each header cell and data cell that's non-English gets the translation.

Therefore, the final answer should have all the Chinese phrases translated, with their English equivalents in parentheses, while keeping the original structure.
</think>

| 全宗号 (Collection Number) | 全宗名称 (Collection Name) | 案卷起止时间 (Case File Start and End Time) | 案卷数量（卷、件） (Case File Quantity (Volumes, Items)) |
| --- | --- | --- | --- |
| XW024 | 北京市宣武区饮食公司★ (Beijing Xuanwu District Catering Company★) | 1956~1999 | 2331卷 (2331 volumes) |
| XW025 | 北京市宣武区土产杂品公司★ (Beijing Xuanwu District Local Products Company★) | 1965~2000 | 1277卷 (1277 volumes) |
| XW026 | 北京市宣武区广安门外街道 (Beijing Xuanwu District Guang'anmen Subdistrict) | 1958~2010 | 3254卷 (3254 volumes) 2643件 (2643 items) |
| XW027 | 北京市宣武区副食品公司★ (Beijing Xuanwu District Quasi-Food Company★) | 1957~1999 | 3488卷 (3488 volumes) |
| XW028 | 北京市宣武区糖业烟酒管理处★ (Beijing Xuanwu District Sugar and Liquor Administration Office★) | 1963~1965 | 115卷 (115 volumes) |
| XW029 | 北京市宣武区修理公司★ (Beijing Xuanwu District Repair Company★) | 1961~1999 | 1170卷 (1170 volumes) |
| XW030 | 北京市宣武区教育局 (Beijing Xuanwu District Education Bureau) | 1959~2010 | 3944卷 (3944 volumes) 3467件 (3467 items) |
| XW031 | 北京市宣武区牛街街道 (Beijing Xuanwu District Niujie Subdistrict) | 1958~2010 | 4163卷 (4163 volumes) 2538件 (2538 items) |
| XW032 | 北京市宣武区粮食局 (Beijing Xuanwu District Grain Bureau) | 1955~1999 | 2032卷 (2032 volumes) |
| XW033 | 北京市宣武区煤炭公司★ (Beijing Xuanwu District Coal Company★) | 1955~2002 | 1853卷 (1853 volumes) |
| XW034 | 北京市宣武区服装公司★ (Beijing Xuanwu District Clothing Company★) | 1973~1999 | 1793卷 (1793 volumes) |
| XW035 | 北京市宣武区物资回收公司★ (Beijing Xuanwu District Material Recycling Company★) | 1961~1998 | 685卷 (685 volumes) |
| XW036 | 北京市宣武区工商行政管理局 (Beijing Xuanwu District Administration for Industry and Commerce) | 1970~2010 | 1968卷 (1968 volumes) 1275件 (1275 items) |
| XW037 | 北京市宣武区劳动和社会保障局 (Beijing Xuanwu District Labor and Social Security Bureau) | 1972~2010 | 3579卷 (3579 volumes) 28220件 (28220 items) |
| XW038 | 北京市宣武区物资管理局★ (Beijing Xuanwu District Material Management Bureau★) | 1972~1999 | 385卷 (385 volumes) |
| XW039 | 北京市宣武区技术监督局 (Beijing Xuanwu District Technical Supervision Bureau) | 1972~1996 | 282卷 (282 volumes) |
| XW040 | 北京市宣武区广安门内街道 (Beijing Xuanwu District Guang'anmen Inner Subdistrict) | 1958~2010 | 5420卷 (5420 volumes) 2828件 (2828 items) |
| XW041 | 北京市宣武区陶然亭街道 (Beijing Xuanwu District Taoran Pavilion Subdistrict) | 1955~2010 | 4349卷 (4349 volumes) 1733件 (1733 items) |
| XW042 | 中共北京市宣武区委党校 (Communist Party of Beijing Xuanwu District Committee Party School) | 1967~2010 | 467卷 (467 volumes) 662件 (662 items) |
| XW043 | 中共北京市宣武区纪律检查委员会 (Disciplinary Inspection Committee of the Communist Party of Beijing Xuanwu District) | 1985~2010 | 867卷 (867 volumes) 1721件 (1721 items) |
| XW044 | 中国人民政治协商会议北京市宣武区委员会 (Chinese People's Political Consultative Conference Beijing Xuanwu District Committee) | 1956~2010 | 1103卷 (1103 volumes) 3737件 (3737 items) |
| XW045 | 北京市宣武区人事局机关工作委员会 (Beijing Xuanwu District Personnel Bureau Organs Work Committee) | 1985~2010 | 494卷 (494 volumes) 520件 (520 items) |
| XW046 | 北京市宣武区机构编制委员会办公室★ (Beijing Xuanwu District Institutional Compilation Committee Office★) | 1985~2009 | 1866卷 (1866 volumes) 2077件 (2077 items) |
| XW047 | 北京市宣武区档案局（馆） (Beijing Xuanwu District Archives (Museum)) | 1985~2010 | 1088卷 (1088 volumes) 684件 (684 items) |
| XW048 | 北京市宣武区民政局 (Beijing Xuanwu District Civil Affairs Bureau) | 1985~2010 | 8443卷 (8443 volumes) 1643件 (1643 items) |
| XW049 | 人物全宗 (Personnel Collection) |  |  |

