![Navigation List](/uploads/album/Navigation-List.png)

```swift
import SwiftUI

struct ContentView: View {
    var items = ["Item 1", "Item 2", "Item 3"]
    
    var body: some View {
        NavigationView {
            List(items, id:\.self) { item in
                NavigationLink(destination: Text("Detail")) {
                    HStack {
                        Image(systemName: "gift")
                            .foregroundColor(.green)
                        VStack {
                            Text(item)
                                .font(.headline)
                            Text("Subtitle")
                                .font(.subheadline)
                                .foregroundColor(.gray)
                        }
                    }
                }
            }.navigationBarTitle(Text("Navigation View"))
        }
    }
}
```
