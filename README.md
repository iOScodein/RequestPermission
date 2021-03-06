<img src="https://rawcdn.githack.com/IvanVorobei/RequestPermission/fb53d20f152a3e76e053e6af529306611fb794f0/resources/request-permission - baner.svg"/>

## About
This project is about managing permissions with the customizable visual effects. Beautiful dialog increases the chance of approval (which is important when we request notification). Simple control of this module saves you hours of development. You can start using this project with just two lines of code and easy customization! You can see [how I am designed UI](https://youtu.be/1mDdX7fQRv4) and [how use pod tutorial](https://youtu.be/viFDunOdyBg) on youtube

Preview GIF loading `4mb`. Please, wait

<img src="https://rawcdn.githack.com/IvanVorobei/RequestPermission/fb53d20f152a3e76e053e6af529306611fb794f0/resources/request-permission - mockup_preview.gif" width="500">

<img src="https://rawcdn.githack.com/IvanVorobei/RequestPermission/6fcd9bdb50a99cea358294999e161dffe55be46f/resources/request-permission - donate.svg"/>

The project is absolutely free, but but it takes time to support and update it. Your support is very motivating and very important. I often receive emails asking me to update or add functionality. [Small donate](https://money.yandex.ru/to/410012745748312) for a cup of coffee helps to develop the project and make it better

<img src="https://rawcdn.githack.com/IvanVorobei/RequestPermission/6fcd9bdb50a99cea358294999e161dffe55be46f/resources/request-permission - donate.svg"/>

## Requirements
Swift 4.2. Ready for use on iOS 10+

## Integration
Drop in `source/sparrow` folder to your Xcode project. Make sure to enable `Copy items if needed` and `Create groups`

Or via CocoaPods:
```ruby
pod 'SPPermission'
```
## How to use
Call `SPPermission` and use func `request()`. Also passed controller, on which dialog should present
```swift
class ViewController: UIViewController {

    override func viewDidAppear(_ animated: Bool) {
        super.viewDidAppear(animated)
        SPPermission.Dialog.request(with: [.camera, .microphone, .notification], on: self)
    }
}
```
If you want to know if you have received permission, you should call the function:
```swift
let isAvailableCamera = SPPermission.isAllow(.сamera)
```
## Permissions

<img src="https://rawcdn.githack.com/IvanVorobei/RequestPermission/951477c8e89de55eeeac441102b52b1415c691b7/resources/request-permission_permissions.png"/>

## Delegate
To track events hide & allowed permission associated with `SPPermission`, implement the protocol `SPPermissionDialogDelegate` and pass the delegate
```swift
SPPermission.Dialog.request(
    with: [.calendar, .microphone],
    on: self,
    delegate: self
)
```
## DataSource
If you want to change the text, you need to implement the `SPPermissionDialogDataSource` protocol. Redefine the needed parameters to see the changes. In the project you can find an example
```swift
SPPermission.Dialog.request(
    with: [.photoLibrary, .contacts],
    on: self,
    delegate: self,
    dataSource: self
)
```

if you want add or remove close button (for close dialog, need swipe it), you need ovveride parametr  `showCloseButton`

<img src="https://rawcdn.githack.com/IvanVorobei/RequestPermission/b3e613295b73be36c8a3d35126d1f7015ef432a8/resources/request-permission - close button.png"/>

## Apps, using lib
I like the idea to specify applications that use the SPPermission. Please, contact me via email. You can find it in the section `Contacts` so that I added app here

## License
`SPPermission` is released under the MIT license. Check LICENSE.md for details

## Contact
[@ivanvorobei in telegram](https://t.me/ivanvorobei)

[https://hello.ivanvorobei.by](https://hello.ivanvorobei.by)

[https://ivanvorobei.by](https://hello.ivanvorobei.by) 

hello@ivanvorobei.by

my apps [in AppStore](https://itunes.apple.com/us/developer/polina-zubarik/id1434528595) & [in AppStore 2](https://itunes.apple.com/us/developer/mikalai-varabei/id1435792103)

If you need develop application or nice UI, write me
