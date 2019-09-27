![Alert Modal](/uploads/album/Alert-Modal.png)

```swift
import SwiftUI

struct ContentView: View {
    @State private var showingAlert = false

    var body: some View {
        Button(action: {
            self.showingAlert = true
        }) {
            Text("Open")
        }
        .alert(isPresented: $showingAlert) {
            Alert(title: Text("Title"),
                  message: Text("Optional Message"),
                  primaryButton: .destructive(Text("Primary Button")),
                  secondaryButton: .cancel())
        }
    }
}
```
