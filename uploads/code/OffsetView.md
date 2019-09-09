![Offset View](/uploads/album/Offset-View.png)

```swift
import SwiftUI

struct ContentView: View {
    var body: some View {
        VStack {
            Rectangle()
                .foregroundColor(.green)

            Circle()
                .foregroundColor(.blue)
                .offset(y: -130)
                .padding(.bottom, -130)

            VStack(alignment: .leading) {
                Text("Title")
                    .font(.title)
                HStack(alignment: .top) {
                    Text("Subtitle 1")
                        .font(.subheadline)
                    Spacer()
                    Text("Subtitle 2")
                        .font(.subheadline)
                }
            }
            .padding()

            Spacer()
        }
    }
}
```
