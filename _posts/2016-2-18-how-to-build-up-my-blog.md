---
layout: post
title:  "该博客的搭建"
date:    2016-02-18 20:17 +0800
categories: tech
tags: tech
---

以前用pelican搭在github上过，跟着[这个](http://www.lizherui.com/pages/2013/08/17/build_blog.html)教程走的  
pelican是静态博客生成器，自己写的markdown博客，用博客程序pelican把内容转换为静态内容在网上查看(没有后台的动态功能)  
pelican可以转换，可以实时 查看本地 博客文件 编写效果  

后来在阿里云主机上搭建过wordpress并且还有其开发环境，比较麻烦点，后来主机不想续费了，给冲掉了，哎~ 自己的博客的稳定靠谱呀。  

再后来选择用[github pages](https://pages.github.com/)功能，外加官网推荐的jekyll搭建的博客  

---------------  
我搭的是windows，本地安装整理比较麻烦。别人的教程写的很好[windows下搭建教程](http://corey600.github.io/blog/2013/02/28/use-github-and-octopress-create-blog/)

还有一些有趣的[jekyll主题](http://jekyllthemes.org/)

官网上和中文教程都有，不用多说

### 我想xujiazhe.info 和 www.xujiazhe.info 都能访问我的博客

#### 1 配置dns服务器里面的这两条记录。

![这里][1]

#### 2 在CNAME文件里面写下下面的内容

www.xujiazhe.info  
xujiazhe.info


### 我想用jetbrains的IDE来写博客

#### 1  为markdown文件类型添加一个后缀 md
 ![这里][2]

#### 2 添加一个博文的模板，创建md的时候就自动模板了。名字叫 Markdown File


{% highlight PHP %}
---
layout: post
title:  "#[[$Title$]]#"
date:    ${YEAR}-${MONTH}-${DAY} ${TIME} +0800
categories: #[[$CATEGORIES$]]#
---
{% endhighlight %}

用的是Apache Velocity模板语言

![这里][3]
[]:

#### 3 新建文件的时候选择Markdown File
![这里][4]

#### 4 新建效果，idea还有个预览插件
![这里][5]  
　　  
　　  

-------------
markdown尾行两个空格是段内换行

[1]:https://lh3.googleusercontent.com/YmxgxIF9F8Ykbs4EYVolVJ968JhNmqnw76mL4qoV1he5W_oh9WqKKBoTSw9xRFMsdTkdV2At6M51ZRpB9W3mJYCga8e5rodZzrbhb-u7bFFrwpQY6NUgu9WA5YW0FZmdWwA2qACRqJcx9_crriTiJMA64kYn27UQzDQK-JzOp82kU2Trz8lA51DbGwmaaQHJB7Z1UTUdP7Kuv8lkSOufCQykOuhGxl8B9KynRR7dBAKvye4avmzbqJ_y6Bt4T0_fo0GenINXOeQzLOMMTlLOOUWRmruSaatHTvnuBpSgZDj8HZ7UC4lLWbRaC54sxRle9-ObBx5siuMAvNeP0t2c381lUERs4EdhohBbMoNQczJa8rRzZrnagerJ68jQ0-KublCtys6fE3-TEILatqi0irQkhCdOSci91F683bIADjMcclb8-eJ_4iEwxu9ZwPRem_B4uCbf9gEa3kRNjGjvho-0vjYxjhLejO3etvGPc1foTOc3wNOWgP95Ssy4NGZhRhWRIDW_ulE_Y6GgVwRejLTGKXaipmW9vviPas30ArcfnrTZ7n9BowGMfIenrGU4q-uH=w790-h634-no
[2]:https://lh3.googleusercontent.com/hbJJWwnEuxzVUy6HRMo47ooiFyyLv9KmdB5chTSrp6VmCQaasGmp5IKTNdOlGtgxVOwprNY_-rmw72IFfk8oxmod7OhFMJTyCNvObiAouzmO0q6gk6BjFwDM1apAvUdXwXZz9iRSCFM1qug9wwlCo8bHrmI_8u0ZIpZ0J9DtZkYIvNXSMAMDIyea2Wrhfyv6AZq7YDXY6F6kSWOrQ_pjlI_XiSGKnYlGHsYlZdtYie9dTOpNFAPqjHZ6CSPox8G0hwn_RNIdIxFQfusToRP5pT0GFifbJyhNpSNpxQrES4QMiLY2XXknN3EBEninQn1NnuvA7dOOxMO-8Kx2HIkLLKcxfvU5TArsXXVTZT1TxIn4yEpA0CLF_vvTNk3kW8NW4MtWaPX-4axmVgOuXuYWGPfRQns3hzlfPhbjswWBIjfhx_JqvH4RRc-7E4lATa4oUpR_uYCCm9brqdjCNHeZLlARlUEEvZr_-hlcLuMlvPwdGF_Crp3cML9Zf9EjJkc-KEO7HKol7MpdO3K_Q7Mxgg0zIzNOzvZ_ueUKlLu4_vR9tRN_bUGEO0gzrvdtDHWqV642=w1038-h701-no
[3]:https://lh3.googleusercontent.com/5p6ilRXDHE7iE3y9nR-5rljJo8g0n3z4U8kM2wfXVCfoINN0intcO3IPVNnlVxxmtF1bI_aZi3sd0l9nf5nA4cjDzPrbl_jsY7-g0l1j0yFdVJlQC6O2pjmMThLBrwfRfsCPXtz82vdO6K_mvIozdBDJp_IdPyAQaKw06iUJ12SDTTgEUWc6b3mfd8ik1XwcEmynmD3mn7HSUL8BjyvUO1ErX4GyHrmXj4SB9nSC_BU-JcRkg765hfZKEMffpNuOyw5ilaqAVvW2eIj6lSM82RUt46CEqkLrkYI83HSwh1tLFgzewOJg_6kvooe68bozyCkfPkDLHE2z2N6tQr4utfOh8XsPLXVGso-Uu2ucT88jqKHN-Q3B8vWnlk9_LnZBvf0q-ph6H565fst536l3VXZhPV1Z3ZcxW6z8bdgo_R-pxQkW0L7JJNxEhtxDjRk0I4PaTmojIAtGS915etUQ8FUP9299lgF9S12gFCJ90NbxpfNDrRtlcxCTJV49zawBMVrH5R0WIlYloiR4XMdGrnuodTZDYoI4cXJiX1LZIybZynCUPMIC97xNX4R1r5Ir-LYf=w1038-h701-no
[4]:https://lh3.googleusercontent.com/KcVOV21Oz_Vf9JH73KDp2jBhrtQQG-epI0VomnF50dGqIik-LZkN5yf0rJyQtOPRIgrQ7KrvualrvEvjGCmFsTTwzRg4kssmEUQ39gX8sFcAeY0OLReiH-iA7fWGADUW785uYPTJZ1_Dr3F3zq6OiJemQLQMV5SXNSfDjO3icEdhe-r3bGJoWQ_ddpjIpZfMQRGwHQ3gqbr3qV6ggSFVGi6hj7FWDM8t1xDFE4IZ_F0QjQEAJchUN7cLiFXQ1hNdRm-aIWhoJ_hSX49on1rDp1TpCxPpow86xduIETpAmOohqi9vg_rjLIss8_2Zoq-rtSpXxNxCeDgcxeNWC2nS3APeynKxLGSTpoD25OJtkOtC99oocgWLAjearJ2vrJv5O_5z0JCSxLqPMguxwLj_v-eTCm8ZmKMiXZ0DUiBTPze0DGNgsTW_P1GYZtl4-MqH7Fx0cEO4NZOJWkBNQgno0zDcEirz5tjMhJD2Jsz7MxJEZDA6WehMU1Xh6oHXBK_tM_fJzIwaLmrVy9JxHiWZpglBrbhOjS6a-qpf_IyabEBHKOlz6cIcwx3J5y2pj625kWLG=w372-h687-no
[5]:https://lh3.googleusercontent.com/WC0R3svvKie2e57K7fWUBz6Q6Q0CDzHGM5-zKzXgOMwlSkBYXR7evmCp3Z-gQzJOirKf_UF7yW36w3XeBhuiIn-JmQLcKjmBc0_y1EIYw2cIdE4oYbs3G2jKP3-sAibSO5u26D4gs8WenbUOqqlRx4Gi0t24ClVGClF_rjTGu_TslckysNe8g1ywG80EnEmoYy-JoFWeBALoZkn57hxhZ8J1oHTd16zwmIdcA48T3sOgW1xGSmqjVWn33ZNfopkVe3NJhAUCuPNyb95lEcirMXeckK3lls2_KHNobwm9wXc8k_CmvsNLcL67O0ViNn329PXX7J7Dcr6H9a-d-m87Bs1GnAS1iB2ZTxqqt2eDXuuxpZkOaRvf70fZ0Tq-eEABK-aMPI29xk6XGYoqncoux0pmAEhn-vsNd30CZp8t-2RZZgaoKuZ40qJGba4wpQ-lAr2RSzPQm_bQtFxPgh3WEUrk5su1LaZz0yQxOJTlM4BHh_WyYDTHlyGpfGmvuq63bCoIC_I-i3--FAGvg0MLZOGT77g3gU3FjXbQnM-GgBl9ROfo60GLtx6YLqJzCgbDxcrB=w816-h712-no


