![Stepper View](/uploads/album/StepperView.png)

```swift
import SwiftUI

struct ContentView: View {
    @State var count: Int = 0
    
    var body: some View {
        Stepper(value: $count,
                in: 0...10,
                label: {Text("Stepper: \(count)") })
            .padding()
    }
}
```
