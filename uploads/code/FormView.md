![Form View](/uploads/album/Form-View.png)

```swift
import SwiftUI

struct ContentView: View {
    static let cities = ["New York", "London", "New Delhi", "Singapore", "Sydney"]

    @State private var citySelected = 0 //0 represents the first item being the default selection
    @State private var addOwnCity = false
    @State private var ownCity = ""

    var body: some View {
        NavigationView {
            Section {
                Form {
                    Picker(selection: $citySelected, label: Text("Choose a city:")) {
                        ForEach(0 ..< Self.cities.count) {
                            Text(Self.cities[$0])
                        }
                    }
                    Toggle(isOn: $addOwnCity.animation()) {
                        Text("Do you want to add your own city?")
                    }
                    if addOwnCity {
                        TextField("Enter your own city" ,text: $ownCity)
                    }
                }
            }.navigationBarTitle(Text("Form example"), displayMode: .inline)
        }
    }
}
```
