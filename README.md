【遭遇問題】Python-Firebase安裝執行後回應SyntaxError
====

錯誤：from .async import process_pool ^ syntaxerror: invalid syntax 
==

![image](https://user-images.githubusercontent.com/46515944/176098422-263613ae-e0eb-4b24-8955-75f6972f2b47.png)

解決方式：
==
將衝突檔名做修正即可，而有哪些檔案需要做調整呢?此外，該檔位於哪個資料夾內呢?
依本次為例，有三個地方需要做修正。

> 1. 其指定資料夾的 async.py，做檔名修正
> 2.  __init__.py 內程式碼 "from .async import process_pool"，.async做更改(看第一步改成什麼檔名)
> 3. firebase.py內程式碼"from .asyncn import process_pool"，與上一步做一樣的更改

該檔位於 C:\Users\s1074532\anaconda3\Lib\site-packages\firebase  (這個console那裏會寫)

![image](https://user-images.githubusercontent.com/46515944/176098627-2c295edf-5012-4873-8b4a-42264ea91875.png)

上圖，為第一個要修正的檔案(黃色標示)，可以在後頭多個n就好。

![image](https://user-images.githubusercontent.com/46515944/176098659-bdff062a-1124-4ccb-ac9c-cb271d131d8e.png)

第二步，__init__.py內的程式碼，把.asycn改成看你剛剛第一步把它換成什麼檔名，像是.asyncnn，多一個n

![image](https://user-images.githubusercontent.com/46515944/176098676-7d563ce3-0479-4b54-b8f0-1bdb6fff4699.png)

第三步同上，將firebase.py內的程式碼，更改一下，即完成囉~~


>本文參考至  <https://b0212066.pixnet.net/blog/post/214531608-firebase%E5%9C%A8python3.7%E5%87%BA%E7%8F%BEsyntaxerror%E9%8C%AF%E8%AA%A4>
