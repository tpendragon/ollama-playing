# Goal

How efficiently can we solve the use case: Convert this image to a human readable format and translate it?

Image: ![image](../chinesetoc.jpg)

# Options

## Docling -> Qwen

Docling (30s)

### Docling + Easy OCR
Convert the image to markdown: `docling --to=md --ocr-lang=en,ch_tra chinesetoc.jpg`

525

| 全宗號   | 全宗名稱                            | 案卷起止時間    |               |
|-------|---------------------------------|-----------|---------------|
| XW024 | 北京市宣武區飲食公司+                     | 1956~1999 | 2331卷         |
| XW025 | 北京市宣武區土產雜品公司+                   | 1965-2000 | 1277卷         |
| XW026 | 北京市宣武區廣安門外街道                    | 1958~2010 | 3254卷 2643 件  |
|       | 北京市宣武區副食品公司+                    | 1957~1999 | 3488卷         |
| XW028 |                                 | 1963~1965 |               |
| XWO29 | 北京市宣武區修理公司+                     | 1961~1999 | ll70卷         |
| XW030 | 北京市宣武區教育局 北京市宣武區教育委員會           | 1959~2010 | 3944卷 3467 件  |
| XW031 | 北京市宣武區牛街街道                      | 1958~2010 | 4163卷 2538 件  |
| XW032 | 北京市宣武區糧食局                       | 1955~1999 | 2032卷         |
| XW033 | 北京市宣武區煤炭公司+                     | 1955~2002 | 1853卷         |
| XW034 | 北京市宣武區服裝公司+                     | 1973~1999 | 1793卷         |
|       | 北京市宣武區物資回收公司+                   | 1961~1998 | 685卷          |
| XW036 | 北京市宣武區工商行政管理局                   | 1970~2010 | 1968卷 1275 件  |
| XW037 | 北京市宣武區勞動和社會保障局 北京市宣武區人力資源和社會保障局 | 1972-2010 | 3579卷 28220 件 |
| XW038 | 北京市宜武區物資管理局+                    | 1972~1999 | 385卷          |
|       | 北京市宣武區技術監督局                     | 1972~1996 | 282卷          |
| XW040 | 北京市宣武區廣安門內街道                    | 1958~2010 | 5420卷 2828 件  |
| XWO41 | 北京市宣武區陶然亭街道                     | 1955-2010 | 4349卷 1733 件  |
| XW042 | 中共北京市宣武區委黨校                     | 1967~2010 | 467卷 662 件    |
| XW043 | 中共北京市宣武區紀律檢查委員會                 | 1985-2010 | 867卷 1721 件   |
|       | 中國人民政治協商會議北京市宣武區委員              | 1956~2010 | 1103卷 3737 件  |
| XW045 |                                 | 1985-2010 | 494卷 520 件    |
| XW046 | 北京市宣武區人事局 北京市宣武區機構編制委員會辦公室+     | 1985~2009 | 1866卷 2077 件  |
| XW047 | 北京市宣武區檔案局(館)                    | 1985~2010 | 1088卷 684 件   |
|       | 北京市宣武區民政局                       | 1985~2010 | 8443卷 1643 件  |
| XW049 | 人物全宗                            |           |               |

### Docling + Tesseract

Very, very bad.

Tried with `docling --to=md --ocr-engine tesseract --output docling_output --ocr-lang=chi_tra+eng chinesetoc.jpg`

### Docling + VLM

This uses a small ML model docling created.

`docling --to=md --output docling_output --ocr-lang=en,ch_tra --pipeline=vlm chinesetoc.jpg`

### Qwen3:4b (43s)

| Fonds Number | Fonds Name | Period of File Dates |          |
|-------------|-----------|----------------------|----------|
| XW024       | Beijing Xuanwu District Food Company+ | 1956-1999 | 2331 volumes |
| XW025       | Beijing Xuanwu District Handicrafts and Commodities Company+ | 1965-2000 | 1277 volumes |
| XW026       | Beijing Xuanwu District Guanshanmenwai Street | 1958-2010 | 3254 volumes 2643 items |
|             | Beijing Xuanwu District Subfood Company+ | 1957-1999 | 3488 volumes |
| XW028       |                               | 1963-1965 |          |
| XW029       | Beijing Xuanwu District Repair Company+ | 1961-1999 | 1170 volumes |
| XW030       | Beijing Xuanwu District Education Bureau Beijing Xuanwu District Education Committee | 1959-2010 | 3944 volumes 3467 items |
| XW031       | Beijing Xuanwu District Niujie Street | 1958-2010 | 4163 volumes 2538 items |
| XW032       | Beijing Xuanwu District Grain Bureau | 1955-1999 | 2032 volumes |
| XW033       | Beijing Xuanwu District Coal Company+ | 1955-2002 | 1853 volumes |
| XW034       | Beijing Xuanwu District Apparel Company+ | 1973-1999 | 1793 volumes |
|             | Beijing Xuanwu District Materials Recycling Company+ | 1961-1998 | 685 volumes |
| XW036       | Beijing Xuanwu District Administration for Industry and Commerce | 1970-2010 | 1968 volumes 1275 items |
| XW037       | Beijing Xuanwu District Labor and Social Security Bureau Beijing Xuanwu District Human Resources and Social Security Bureau | 1972-2010 | 3579 volumes 28220 items |
| XW038       | Beijing Xuanwu District Materials Administration Bureau+ | 1972-1999 | 385 volumes |
|             | Beijing Xuanwu District Technical Supervision Bureau | 1972-1996 | 282 volumes |
| XW040       | Beijing Xuanwu District Guanshanmennei Street | 1958-2010 | 5420 volumes 2828 items |
| XW041       | Beijing Xuanwu District Taoranting Street | 1955-2010 | 4349 volumes 1733 items |
| XW042       | Beijing Xuanwu District Party School | 1967-2010 | 467 volumes 662 items |
| XW043       | Beijing Xuanwu District Discipline Inspection Commission | 1985-2010 | 867 volumes 1721 items |
|             | Chinese People's Political Consultative Conference Beijing Xuanwu District Committee | 1956-2010 | 1103 volumes 3737 items |
| XW045       |                               | 1985-2010 | 494 volumes 520 items |
| XW046       | Beijing Xuanwu District Personnel Bureau Beijing Xuanwu District Institutional Compilation Committee Office+ | 1985-2009 | 1866 volumes 2077 items |
| XW047       | Beijing Xuanwu District Archives Bureau (Archive) | 1985-2010 | 1088 volumes 684 items |
|             | Beijing Xuanwu District Civil Affairs Bureau | 1985-2010 | 8443 volumes 1643 items |
| XW049       | Personal Fonds |           |          |

## Qwen3 30B-A3B (No Thinking) (25s)

`ollama run --verbose hf.co/unsloth/Qwen3-30b-A3B-GGUF:Q4_K_XL "Translate this markdown table to english /no_think: " < chinesetoc.md > docling-qwen-30ba3b-nothink.md`

| Fonds Number | Fonds Name                                      | File Start-End Date |               |
|--------------|-------------------------------------------------|---------------------|---------------|
| XW024        | Beijing Xuanwu District Catering Company+        | 1956~1999           | 2331 files    |
| XW025        | Beijing Xuanwu District Agricultural Products Company+ | 1965-2000           | 1277 files    |
| XW026        | Beijing Xuanwu District Guang'anmen Outer Street | 1958~2010           | 3254 files 2643 items |
|              | Beijing Xuanwu District Subsistence Products Company+ | 1957~1999           | 3488 files    |
| XW028        |                                                 | 1963~1965           |               |
| XWO29        | Beijing Xuanwu District Repair Company+          | 1961~1999           | ll70 files    |
| XW030        | Beijing Xuanwu District Education Bureau Beijing Xuanwu District Education Committee | 1959~2010           | 3944 files 3467 items |
| XW031        | Beijing Xuanwu District Niujie Street            | 1958~2010           | 4163 files 2538 items |
| XW032        | Beijing Xuanwu District Grain Bureau             | 1955~1999           | 2032 files    |
| XW033        | Beijing Xuanwu District Coal Company+            | 1955~2002           | 1853 files    |
| XW034        | Beijing Xuanwu District Clothing Company+        | 1973~1999           | 1793 files    |
|              | Beijing Xuanwu District Material Recycling Company+ | 1961~1998           | 685 files     |
| XW036        | Beijing Xuanwu District Administration for Industry and Commerce | 1970~2010           | 1968 files 1275 items |
| XW037        | Beijing Xuanwu District Human Resources and Social Security Bureau Beijing Xuanwu District Human Resources and Social Security Bureau | 1972-2010           | 3579 files 28220 items |
| XW038        | Beijing Xuanwu District Material Bureau+          | 1972~1999           | 385 files     |
|              | Beijing Xuanwu District Technical Supervision Bureau | 1972~1996           | 282 files     |
| XW040        | Beijing Xuanwu District Guang'anmen Inner Street | 1958~2010           | 5420 files 2828 items |
| XWO41        | Beijing Xuanwu District Taoran Pavilion Street   | 1955-2010           | 4349 files 1733 items |
| XW042        | CPC Beijing Xuanwu District Party School         | 1967~2010           | 467 files 662 items |
| XW043        | CPC Beijing Xuanwu District Discipline Inspection Commission | 1985-2010           | 867 files 1721 items |
|              | Chinese People's Political Consultative Conference Beijing Xuanwu District Committee | 1956~2010           | 1103 files 3737 items |
| XW045        |                                                 | 1985-2010           | 494 files 520 items |
| XW046        | Beijing Xuanwu District Personnel Bureau Beijing Xuanwu District Institutional Compilation Committee Office+ | 1985~2009           | 1866 files 2077 items |
| XW047        | Beijing Xuanwu District Archives Bureau (Museum) | 1985~2010           | 1088 files 684 items |
|              | Beijing Xuanwu District Civil Affairs Bureau     | 1985~2010           | 8443 files 1643 items |
| XW049        | Personal Fonds                                   |                     |               |

