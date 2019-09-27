![List Background Color](/uploads/album/List-Background-Color.png)

```swift
import SwiftUI

struct ContentView: View {
    var body: some View {
        List {
            ForEach(1...100, id: \.self) { i in
                Text("\(i)")
                    .listRowBackground( (i % 2 == 0) ? Color.clear : Color.green )
            }
        }
    }
}

```
