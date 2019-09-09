![Circle Image](/uploads/album/Circle-Image.png)

```swift
import SwiftUI

struct ContentView: View {
    var body: some View {
        Image(systemName: "photo")
            .resizable()
            .aspectRatio(1, contentMode: .fit)
            .foregroundColor(.green)
            .clipShape(Circle())
            .overlay(
                Circle().stroke(Color.white, lineWidth: 4))
            .shadow(radius: 10)
            .padding()
    }
}
```
