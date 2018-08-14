易源（http://www.showapi.com）
一个api聚合网站，提供统一的接口调用协议来为开发者提供Api服务
个人用golang写的api调用SDK

初始化
-----------
		   go get git.oschina.net/myml/showSdk

例子
-----------

//	examples  project examples.go
	package main

	import (
		"fmt"
		"showSdk"
	)

	func main() {
		sa := showSdk.NewShowApi(162, "ade009*************e8d1c398")
		sa.AddFile("src_img", "0.jpg")
		sa.AddFile("logo_img", "0.jpg")
		sa.Add("xy", "+50")
		fmt.Println(sa.Post("http://route.showapi.com/1-2"))
	}
