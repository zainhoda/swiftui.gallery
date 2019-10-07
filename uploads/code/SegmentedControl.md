![Segmented Control](/uploads/album/Segmented-Control.png)


```swift
import SwiftUI

struct ContentView: View {
    static let ageRanges = ["1-10", "11-18", "18-55", "55+"]
    @State var selectedAgeRange = 0
    var body: some View {
        Picker(selection: $selectedAgeRange, label: Text("Range:")) {
            ForEach(0 ..< Self.ageRanges.count) {
                Text(Self.ageRanges[$0])
            }
        }
        .pickerStyle(SegmentedPickerStyle())
        .padding()
    }
}
```
