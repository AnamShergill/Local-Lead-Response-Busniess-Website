# 🚀 Localhost Development Setup

## Quick Start

### Option 1: NPM Dev Server (Recommended)

```bash
npm run dev
```

This will:
- ✅ Start a local server on `http://localhost:3000`
- ✅ Open your browser automatically to `index.html`
- ✅ Auto-reload on file changes (live reload)
- ✅ No installation needed (uses npx)

### Option 2: Open Demo Page Directly

```bash
npm run demo
```

Opens directly to the demo/form page at `http://localhost:3000/demo.html`

---

## 📋 Available Commands

| Command | What It Does | URL |
|---------|--------------|-----|
| `npm run dev` | Start dev server (homepage) | http://localhost:3000 |
| `npm run start` | Same as dev | http://localhost:3000 |
| `npm run demo` | Open demo page | http://localhost:3000/demo.html |

---

## 🔧 Manual Setup (If npm run dev doesn't work)

### Method 1: Using Python

```bash
# Navigate to project folder
cd c:\Users\Bruno\Desktop\projects\lead-response

# Start server
python -m http.server 8000
```

Then open: `http://localhost:8000`

### Method 2: Using Node.js http-server

```bash
# Install http-server globally (one time)
npm install -g http-server

# Start server
http-server -p 3000 -o
```

Then open: `http://localhost:3000`

### Method 3: Using VS Code Live Server Extension

1. Install "Live Server" extension in VS Code
2. Right-click on `index.html`
3. Select "Open with Live Server"

---

## 🌐 Access Your Pages

Once server is running:

- **Homepage:** http://localhost:3000/index.html
- **Demo/Form Page:** http://localhost:3000/demo.html
- **Styles:** http://localhost:3000/styles.css

---

## 🧪 Testing the Form

### On Localhost:

1. Start dev server: `npm run dev`
2. Navigate to demo page: http://localhost:3000/demo.html
3. Fill out the form
4. Submit and watch:
   - ✅ Success message appears
   - ✅ Loading spinner shows
   - ✅ Redirects to GHL after 2 seconds
5. Check browser console (F12) for logs

### What Works on Localhost:

- ✅ All styling and animations
- ✅ Form validation
- ✅ Button states and loading
- ✅ Success/error messages
- ✅ Redirect to GHL scheduling
- ✅ Mobile responsive testing
- ⚠️ Email sending (may have CORS issues)

### What May Not Work:

- ⚠️ FormSubmit.co (CORS restrictions on localhost)
- ⚠️ Web3Forms (may require production domain)
- ⚠️ Some external API calls

**Solution:** Email services work fine once deployed to production domain.

---

## 📱 Test on Mobile Device

### Same Network Method:

1. Start dev server on your computer
2. Find your computer's IP address:
   ```bash
   ipconfig
   ```
   Look for "IPv4 Address" (e.g., 192.168.1.100)

3. On your phone, open browser and go to:
   ```
   http://192.168.1.100:3000
   ```

### Using ngrok (Expose to Internet):

```bash
# Install ngrok
npm install -g ngrok

# Start your dev server first
npm run dev

# In another terminal, expose it
ngrok http 3000
```

You'll get a public URL like: `https://abc123.ngrok.io`

---

## 🔍 Debugging on Localhost

### Browser Console:

1. Press `F12` to open DevTools
2. Go to **Console** tab
3. Submit form and watch for:
   - "Email sent successfully via FormSubmit"
   - "Form submission completed"
   - "Redirecting to GHL scheduling"

### Network Tab:

1. Press `F12` → **Network** tab
2. Submit form
3. Check API calls to:
   - FormSubmit.co
   - Web3Forms
   - GHL webhook

### Common Issues:

| Issue | Solution |
|-------|----------|
| Port already in use | Change port: `npx live-server --port=8080` |
| CORS errors | Normal on localhost, works in production |
| Files not loading | Check file paths are relative |
| CSS not applying | Hard refresh: `Ctrl + Shift + R` |

---

## 🎨 Live Reload

The dev server automatically reloads when you edit:
- ✅ HTML files
- ✅ CSS files
- ✅ JavaScript (embedded in HTML)

Just save your file and the browser refreshes!

---

## 🚀 Quick Test Checklist

- [ ] Run `npm run dev`
- [ ] Browser opens automatically
- [ ] Homepage loads correctly
- [ ] Navigate to demo page
- [ ] Form displays properly
- [ ] Fill out test data
- [ ] Submit form
- [ ] Success message appears
- [ ] Loading spinner shows
- [ ] Redirects to GHL after 2 seconds
- [ ] Check console for logs
- [ ] Test on mobile (optional)

---

## 💡 Pro Tips

1. **Keep terminal open** - Don't close the terminal running the server
2. **Use incognito mode** - Avoids cache issues
3. **Check console first** - Most issues show up there
4. **Test responsive** - Use browser DevTools device toolbar
5. **Clear cache** - If styles don't update: `Ctrl + Shift + R`

---

## 🛑 Stop the Server

Press `Ctrl + C` in the terminal running the server

---

## 📦 No Installation Required

The `npm run dev` command uses `npx` which:
- ✅ Downloads live-server temporarily
- ✅ No global installation needed
- ✅ Works immediately
- ✅ Clean and simple

---

## 🎯 Ready to Test!

Just run:
```bash
npm run dev
```

Your website will open at `http://localhost:3000` 🚀

---

**Need help?** Check the browser console (F12) for any errors.
