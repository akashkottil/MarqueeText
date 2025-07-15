# 🌀 MarqueeText for SwiftUI

A lightweight and reusable SwiftUI component that creates a **horizontal scrolling (marquee-style)** animation for long text. This is especially useful in lists, dashboards, and compact UIs where text might overflow or get truncated.

---

## 🚀 Features

- 🔁 Smooth horizontal scrolling animation
- 🧠 Automatically scrolls only if the text exceeds a configurable length (`> 8` by default)
- 📏 Adaptive to parent view width
- 🎯 Perfect for flight info rows, tickers, and constrained UIs
- 💡 Easy to integrate and customize

---

## 📦 Installation

### Manual

Just copy the following two files into your SwiftUI project:

- `MarqueeText.swift`
- `WidthPreferenceKey.swift` (if needed for advanced dynamic width logic)

---

## 🛠 Usage

### Step 1: Import and Use in Your View

```swift
MarqueeText(text: "Air India Express Flight to Dubai", font: .system(size: 14))
    .fontWeight(.semibold)
    .foregroundColor(.gray)
    .frame(height: 20)
Step 2: Optional - Use it in a List or Custom Row
swift
Copy
Edit
HStack {
    MarqueeText(text: flight.airline, font: .system(size: 14))
        .fontWeight(.semibold)
        .foregroundColor(.gray)
        .frame(height: 20)
}
⚙️ Parameters
Parameter	Type	Default	Description
text	String	—	The text to display and animate
font	Font	.body	The font style of the text
duration	Double	6.0	The animation scroll duration
delay	Double	1.0	Delay before scrolling starts
threshold	Int	8	Minimum text length to trigger scrolling

📸 Preview
📷 You can add a GIF or image preview here:

✅ Example Use Case
This is ideal for:

Airline or transport apps with long carrier names

Stock tickers or news banners

Compact list items where full text visibility is needed

🤝 Contributions
Feel free to open issues or submit pull requests to improve the animation behavior, add new features like pause on tap, or make it accessible.

🧑‍💻 Author
Made with ❤️ by Akash Kottil

📄 License
This project is licensed under the MIT License.

yaml
Copy
Edit

---

Let me know if you'd like:
- A demo SwiftUI preview app setup for testing
- A GIF for the animation (you can record one using QuickTime or a tool like Kap)
- Integration with Swift Package Manager (SPM) if you want to share it as a package!
