![Social Image Card](/uploads/album/Social-Image-Card.png)

```swift
import SwiftUI

struct ContentView: View {
    @State var image: Image = Image(systemName: "photo")
    @State var upvoted: Bool = false
    @State var numVotes: Int = 1
    @State var numComments: Int = 3
            
    private let colors = [
        Color.white,
        Color.green,
        Color.blue
    ]

    var body: some View {
        
        VStack(alignment: .center) {
            HStack {
                Text("Title")
                    .font(.system(size: 30))
                    .fontWeight(.heavy)
                    .foregroundColor(.yellow)
                Spacer()
                Text("Subtitle 1")
                    .font(.subheadline)
                    .foregroundColor(.black)
            }
            Button(action: {
            }) {
                self.image
                .renderingMode(Image.TemplateRenderingMode?.init(Image.TemplateRenderingMode.original))
                    .resizable()
                    .scaledToFit()
                    .clipShape(RoundedRectangle(cornerRadius: 10))
                    .overlay(RoundedRectangle(cornerRadius: 10)
                                .stroke(Color.gray, lineWidth: 0))
                    .shadow(radius: 10)
            }
            ZStack {
            HStack {
                HStack {
                    HStack {
                        Image(systemName: "arrow.up")
                        Text("\(numVotes)").transition(.slide)
                    }
                    HStack {
                        Image(systemName: "bubble.right")
                        Text("\(numComments)")
                    }
                }.foregroundColor(.black)
                Spacer()
                Button(action: { self.upvoted.toggle() }) {
                    if self.upvoted {
                        Image(systemName: "arrow.up")
                            .foregroundColor(.purple)
                    } else {
                        Image(systemName: "arrow.up")
                        .foregroundColor(.blue)
                    }
                }.padding(5)
                    .background(self.upvoted ? .green : Color.clear)
                .clipShape(RoundedRectangle(cornerRadius: 5))
            }
            Text("Subtitle 2")
                .font(.caption)
                .foregroundColor(.black)
            }}.padding()
            .background(LinearGradient(gradient: Gradient(colors: colors),
                                       startPoint: .bottom, endPoint: .top))
            .clipShape(RoundedRectangle(cornerRadius: 10))
            .overlay(RoundedRectangle(cornerRadius: 10)
                        .stroke(Color.gray, lineWidth: 0))
            .shadow(radius: 10)
    }
}
```
