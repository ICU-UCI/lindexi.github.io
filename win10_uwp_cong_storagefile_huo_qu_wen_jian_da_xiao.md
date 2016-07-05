# win10 uwp 从StorageFile获取文件大小

本文主要：获取文件大小

        private async Task<ulong> FileSize(Windows.Storage.StorageFile file)
        {
            var size = await file.GetBasicPropertiesAsync();
            return size.Size;
        }//32ddd4227a66713e1329214424c4be9b
        
在群里看到有大神问我就写出，虽然少，在没看到他们说之前没想到，九幽开发者：53078485

参见：http://stackoverflow.com/questions/14168439/how-to-get-file-size-in-winrt
        
<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="知识共享许可协议" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a><br />本作品采用<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">知识共享署名-非商业性使用-相同方式共享 4.0 国际许可协议</a>进行许可。欢迎转载、使用、重新发布，但务必保留文章署名[林德熙](http://blog.csdn.net/lindexi_gd)(包含链接:http://blog.csdn.net/lindexi_gd )，不得用于商业目的，基于本文修改后的作品务必以相同的许可发布。如有任何疑问，请与我[联系](mailto:lindexi_gd@163.com)。        