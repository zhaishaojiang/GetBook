问题：给 [http://abc.com/info](http://abc.com/info) 配置的子路由 [http://abc.com/info/:status，如](http://abc.com/info/:status，如) [http://abc.com/info/audited](http://abc.com/info/audited)   \(audited是info的参数\)无法直接访问，会出现文件路径问题。（如：访问 [http://abc.com/info/audited 时，webpack打包的文件路径会变成http://abc.com/info/\*\*\*）](http://abc.com/info/audited时，webpack打包的文件路径会变成http://abc.com/info/***）)

解决：在 webpack配置文件中设置 output.publicPath = '/'

