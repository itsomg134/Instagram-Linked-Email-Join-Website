#  Instagram Linked Email Join Website

A modern, responsive landing page that collects email addresses and Instagram handles to build a community waitlist. Perfect for creators, brands, or influencers launching new products or exclusive content.

<img width="1885" height="1108" alt="image" src="https://github.com/user-attachments/assets/68b67680-5340-4b5b-95ef-1ebb199bf064" />

##  Features

- Modern UI – Gradient Instagram-inspired design with smooth animations
- Fully Responsive – Works flawlessly on desktop, tablet, and mobile devices
- Email Collection – Validates email format before submission
- Instagram Handle Support – Optional field to collect usernames for DM updates
- LocalStorage Demo – Simulates backend storage (ready for real API integration)
- Real-time Validation – Instant feedback with success/error messages
- Instagram Link – Direct link to your Instagram profile
- Loading States – Button spinner feedback during submission


##  Technologies Used

- **HTML5** – Semantic structure
- **CSS3** – Flexbox, Grid, custom properties, gradients
- **JavaScript (ES6+)** – Form handling, validation, async operations
- **Font Awesome 6** – Icon library
- **Google Fonts (Inter)** – Modern typography

##  Installation

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/instagram-join-page.git
cd instagram-join-page
```

### 2. Open the file

Simply open `index.html` in your browser:

```bash
# On macOS
open index.html

# On Windows
start index.html

# On Linux
xdg-open index.html
```

### 3. (Optional) Run with a local server

For the best experience, use a local development server:

```bash
# Using Python 3
python -m http.server 8000

# Using Node.js (live-server)
npx live-server
```

Then visit `http://localhost:8000`

## 🔧 Customization

### Update Instagram Profile Link

Locate this line in the JavaScript section:

```javascript
const INSTAGRAM_URL = 'https://www.instagram.com/joincreativelab/';
```

Replace with your actual Instagram profile URL.

### Change Brand Colors

Modify the gradient in the `.hero-gradient` and `.join-button` CSS classes:

```css
.hero-gradient {
  background: linear-gradient(135deg, #feda75 0%, #fd5949 45%, #d6249f 80%, #285aeb 100%);
}
```

### Connect to a Real Backend

Replace the `submitJoinRequest` function in the JavaScript with an actual API call:

```javascript
async function submitJoinRequest(email, instagramHandle) {
  const response = await fetch('https://your-api.com/waitlist', {
    method: 'POST',
    headers: { 'Content-Type': 'application/json' },
    body: JSON.stringify({ email, instagramHandle })
  });
  
  if (!response.ok) throw new Error('Submission failed');
  return response.json();
}
```

### Disable LocalStorage Demo

Remove or comment out the localStorage logic in `submitJoinRequest` and replace with your own storage mechanism.

##  Project Structure

```
instagram-join-page/
├── index.html          # Main landing page (HTML, CSS, JS)
├── README.md           # Project documentation
└── assets/             # (Optional) Images, fonts, etc.
```

##  Use Cases

- **Product Launches** – Build hype before releasing a new product
- **Newsletter Signup** – Grow your email list with Instagram integration
- **Event Registration** – Collect attendees with social handles
- **Creator Communities** – Build a waitlist for exclusive content
- **Beta Testing** – Gather early adopters for your app or service

##  Form Validation Details

| Field | Validation | Required |
|-------|------------|----------|
| Email | Standard email format (`name@domain.com`) | ✅ Yes |
| Instagram Handle | Alphanumeric, underscores, periods (1-30 chars) | ❌ No |

##  Browser Support

| Chrome | Firefox | Safari | Edge | iOS Safari | Chrome Android |
|--------|---------|--------|------|------------|----------------|
| Latest | Latest  | Latest |Latest|    Latest  |      Latest    |

##  Contributing

Contributions are welcome! Here's how:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

##  License

This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.

##  Acknowledgments

- Icons by [Font Awesome](https://fontawesome.com/)
- Fonts by [Google Fonts](https://fonts.google.com/)
- Instagram brand assets belong to Meta Platforms, Inc.

##  Contact

Om Gedam

GitHub: [https://github.com/itsomg134](https://github.com/itsomg134)

Email: [omgedam123098@gmail.com](mailto:omgedam123098@gmail.com)

Twitter (X): [https://twitter.com/omgedam](https://twitter.com/omgedam)

LinkedIn: [https://linkedin.com/in/omgedam](https://linkedin.com/in/omgedam)

Portfolio: [https://ogworks.lovable.app](https://ogworks.lovable.app)
