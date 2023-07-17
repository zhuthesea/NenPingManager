# NenPingManager
based on Apple SimplePing, you can use it to ping multiple hosts at once.

```
//Podfile
platform :ios, '11.0'
target 'testPing' do
  pod 'NenPingManager', '~> 0.0.3'

end

```

```
//uts app-ios config.json
{
	"deploymentTarget": "11.0",   
	"dependencies-pods": [
        {
            "name": "NenPingManager",  
            "version": "0.0.3"     
        }
    ]
}
```


```
//vue
    let hosts = ["www.bilibili.com", "www.baidu.com", "www.youku.com", "www.hao123.com"]
    getFastestAddress(hosts, function(fastHost, addressLists, ms) {
        console.log("getFastestAddress", fastHost, addressLists, ms)
    })
```

```
//uts
export function getFastestAddress(addressList : string[], completionHandler : (fastHost ?: string, addressList ?: any[], ms ?: number) => void) {
	NENPingManagerInstance.getFatestAddress(addressList, completionHandler = (fastHost ?: string, addressList ?: any[], ms ?: number) => {
		console.log("uts res", fastHost, addressList, ms)
		completionHandler(fastHost, addressList, ms)
	})

}
```