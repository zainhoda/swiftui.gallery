![TabBar View](/uploads/album/TabBar-View.png)


```swift
import SwiftUI

struct TabBarView: View {
    var body: some View {
        TabView {
            Tab1View()
                .tabItem {
                    Image(systemName: "list.dash")
                    Text("Tab 1")
            }

            Tab2View()
                .tabItem {
                        Image(systemName: "square.and.pencil")
                        Text("Tab 2")
                }
        }
    }
}
```

Change the method in the `SceneDelegate.swift` file to this:
```swift
func scene(_ scene: UIScene, willConnectTo session: UISceneSession, options connectionOptions: UIScene.ConnectionOptions) {
        // Use this method to optionally configure and attach the UIWindow `window` to the provided UIWindowScene `scene`.
        // If using a storyboard, the `window` property will automatically be initialized and attached to the scene.
        // This delegate does not imply the connecting scene or session are new (see `application:configurationForConnectingSceneSession` instead).

        // Create the SwiftUI view that provides the window contents.
        let contentView = TabBarView()

        // Use a UIHostingController as window root view controller.
        if let windowScene = scene as? UIWindowScene {
            let window = UIWindow(windowScene: windowScene)
            window.rootViewController = UIHostingController(rootView: contentView)
            self.window = window
            window.makeKeyAndVisible()
        }
    }
```


```swift
import SwiftUI

struct Tab1View: View {
    var body: some View {
        Text("This is the first tab")
    }
}
```


```swift
import SwiftUI

struct Tab2View: View {
    var body: some View {
        Text("This is the second tab")
    }
}
```
