![ZStack Example](/uploads/album/ZStack-Example.png)

```swift
import SwiftUI

struct ContentView: View {
    var body: some View {
        ZStack {
            Image(systemName: "flame.fill")
                .font(.system(size: 300))
                .foregroundColor(.orange)
            Text("ZStack\nText\non\nImage")
                .font(.largeTitle)
                .multilineTextAlignment(.center)
                .foregroundColor(.blue)
        }
    }
}

```
