import SwiftUI

struct MarqueeText: View {
    let text: String
    var font: Font = .body
    var duration: Double = 6.0
    var delay: Double = 1.0
    var threshold: Int = 8  // ⬅️ only scroll if text count exceeds this

    @State private var textSize: CGSize = .zero
    @State private var animate: Bool = false

    var body: some View {
        GeometryReader { geo in
            let containerWidth = geo.size.width

            if text.count > threshold {
                // Marquee animation
                ZStack {
                    HStack(spacing: 30) {
                        Text(text)
                            .font(font)
                            .background(
                                GeometryReader { textGeo in
                                    Color.clear
                                        .onAppear {
                                            textSize = textGeo.size
                                            animate = true
                                        }
                                }
                            )
                            .fixedSize()

                        Text(text)
                            .font(font)
                            .fixedSize()
                    }
                    .offset(x: animate ? -textSize.width - 30 : 0)
                    .animation(
                        animate
                        ? Animation.linear(duration: duration)
                            .delay(delay)
                            .repeatForever(autoreverses: false)
                        : .default,
                        value: animate
                    )
                }
                .frame(width: containerWidth, alignment: .leading)
                .clipped()
            } else {
                // Static text
                Text(text)
                    .font(font)
                    .lineLimit(1)
                    .truncationMode(.tail)
                    .frame(width: containerWidth, alignment: .leading)
            }
        }
        .frame(height: 20)
    }
}
