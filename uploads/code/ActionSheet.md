![Action Sheet](/uploads/album/Action-Sheet.png)

```swift
import SwiftUI

struct ContentView: View {
    @State private var showingSheet = false

    var body: some View {
        Button(action: {
            self.showingSheet = true
        }) {
            Text("Open")
        }
        .actionSheet(isPresented: $showingSheet) {
            ActionSheet(title: Text("What action?"),
                        message: Text("Pick one"),
                        buttons: [ .default(Text("Option 1"))
                            , .default(Text("Option 2"))
                            , .cancel()
                        ])
        }
    }
}
```
