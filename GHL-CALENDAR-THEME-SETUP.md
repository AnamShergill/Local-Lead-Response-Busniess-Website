# 🎨 GHL Calendar Theme Customization Guide

## ✅ CHANGES MADE

### 1. **Increased Calendar Height**
- **Desktop:** 700px → 900px
- **Mobile:** 650px → 850px
- **Reason:** Ensures submit button is fully visible

### 2. **Added Theme URL Parameters**
Added color parameters to iframe URL:
```
?primaryColor=%234A9EFF&accentColor=%23FF7A00&backgroundColor=%23ffffff&textColor=%230a2d6e
```

**Colors:**
- Primary: `#4A9EFF` (Light Blue)
- Accent: `#FF7A00` (Orange)
- Background: `#ffffff` (White)
- Text: `#0a2d6e` (Dark Blue)

### 3. **Enabled Scrolling**
- Changed `scrolling="no"` to `scrolling="yes"`
- Ensures all content including submit button is accessible

### 4. **Added Custom CSS Injection**
JavaScript attempts to inject custom styles (if allowed by browser)

---

## 🎨 COMPLETE THEME SETUP IN GHL

Since the calendar is in an iframe, the **best way** to customize it is through GoHighLevel settings:

### Step 1: Access Calendar Settings

1. Log into your GoHighLevel account
2. Go to **Calendars** in the left sidebar
3. Find your calendar: "LLR Booking" or similar
4. Click **Settings** or **Edit**

### Step 2: Customize Appearance

Look for **Appearance**, **Theme**, or **Branding** section:

#### **Primary Color** (Buttons, Selected Items)
```
#4A9EFF
```
Use for:
- Submit button background
- Selected date background
- Selected time slot
- Active states

#### **Accent Color** (Hover, Focus)
```
#FF7A00
```
Use for:
- Button hover states
- Links
- Highlights
- Call-to-action elements

#### **Background Color**
```
#ffffff
```
Use for:
- Main background
- Card backgrounds
- Input backgrounds

#### **Text Color**
```
#0a2d6e
```
Use for:
- Headings
- Body text
- Labels
- Form text

#### **Border Color** (Optional)
```
#e2e8f0
```
Use for:
- Input borders
- Card borders
- Dividers

### Step 3: Button Styling

If GHL allows custom button styling:

**Submit Button:**
- Background: `#FF7A00`
- Text Color: `#ffffff`
- Border Radius: `12px`
- Padding: `14px 32px`
- Font Weight: `600`
- Font Size: `16px`

**Button Hover:**
- Background: `#ff9933` (lighter orange)
- Shadow: `0 8px 24px rgba(255, 122, 0, 0.4)`
- Transform: `translateY(-2px)`

### Step 4: Typography

**Font Family:**
```
Inter, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif
```

**Heading Font:**
```
Sora, Inter, sans-serif
```

**Font Sizes:**
- Heading: `24px` - `28px`
- Body: `15px` - `16px`
- Labels: `14px`
- Small text: `13px`

### Step 5: Spacing & Layout

**Border Radius:**
- Buttons: `12px`
- Inputs: `8px`
- Cards: `12px`
- Calendar days: `8px`

**Padding:**
- Buttons: `14px 32px`
- Inputs: `12px 16px`
- Cards: `24px`

---

## 🔧 ALTERNATIVE: Custom CSS (Advanced)

If GHL supports custom CSS injection:

```css
/* Submit Button */
button[type="submit"],
.submit-button,
.book-button,
.appointment-button {
    background: linear-gradient(135deg, #FF7A00 0%, #ff9933 100%) !important;
    color: #ffffff !important;
    border: none !important;
    border-radius: 12px !important;
    padding: 14px 32px !important;
    font-weight: 600 !important;
    font-size: 16px !important;
    font-family: 'Inter', sans-serif !important;
    cursor: pointer !important;
    transition: all 0.3s ease !important;
    box-shadow: 0 4px 12px rgba(255, 122, 0, 0.2) !important;
}

button[type="submit"]:hover,
.submit-button:hover,
.book-button:hover {
    transform: translateY(-2px) !important;
    box-shadow: 0 8px 24px rgba(255, 122, 0, 0.4) !important;
    background: linear-gradient(135deg, #ff9933 0%, #ffaa55 100%) !important;
}

/* Selected Calendar Day */
.calendar-day.selected,
.day.selected,
.date-selected {
    background: #4A9EFF !important;
    color: #ffffff !important;
    border-color: #4A9EFF !important;
}

/* Selected Time Slot */
.time-slot.selected,
.time-selected,
.slot-selected {
    background: #4A9EFF !important;
    border-color: #4A9EFF !important;
    color: #ffffff !important;
}

/* Input Fields */
input[type="text"],
input[type="email"],
input[type="tel"],
select,
textarea {
    border: 1px solid #e2e8f0 !important;
    border-radius: 8px !important;
    padding: 12px 16px !important;
    font-size: 15px !important;
    font-family: 'Inter', sans-serif !important;
    transition: all 0.3s ease !important;
}

input:focus,
select:focus,
textarea:focus {
    border-color: #4A9EFF !important;
    box-shadow: 0 0 0 3px rgba(74, 158, 255, 0.1) !important;
    outline: none !important;
}

/* Headings */
h1, h2, h3, h4 {
    color: #0a2d6e !important;
    font-family: 'Sora', 'Inter', sans-serif !important;
}

/* Body Text */
p, span, label {
    color: #4a5568 !important;
    font-family: 'Inter', sans-serif !important;
}

/* Calendar Container */
.calendar-container,
.booking-calendar {
    background: #ffffff !important;
    border-radius: 12px !important;
}

/* Time Slots */
.time-slot,
.time-option {
    border: 2px solid #e2e8f0 !important;
    border-radius: 8px !important;
    padding: 12px !important;
    transition: all 0.3s ease !important;
}

.time-slot:hover,
.time-option:hover {
    border-color: #4A9EFF !important;
    background: rgba(74, 158, 255, 0.05) !important;
}

/* Calendar Days */
.calendar-day,
.day {
    border-radius: 8px !important;
    transition: all 0.3s ease !important;
}

.calendar-day:hover,
.day:hover {
    background: rgba(74, 158, 255, 0.1) !important;
}

/* Loading States */
.loading,
.spinner {
    border-color: rgba(74, 158, 255, 0.2) !important;
    border-top-color: #4A9EFF !important;
}
```

---

## 📋 QUICK SETUP CHECKLIST

- [ ] Log into GoHighLevel
- [ ] Navigate to Calendar Settings
- [ ] Set Primary Color: `#4A9EFF`
- [ ] Set Accent Color: `#FF7A00`
- [ ] Set Background: `#ffffff`
- [ ] Set Text Color: `#0a2d6e`
- [ ] Customize button styling
- [ ] Set font family to Inter/Sora
- [ ] Adjust border radius to 12px
- [ ] Save changes
- [ ] Test calendar on website
- [ ] Verify submit button is visible
- [ ] Check colors match website
- [ ] Test on mobile device

---

## 🎨 COLOR REFERENCE

Your website uses these colors:

| Element | Color | Hex Code |
|---------|-------|----------|
| Dark Blue (Primary) | Navy | `#061B49` |
| Medium Blue | Blue | `#0a2d6e` |
| Light Blue (Accent) | Sky Blue | `#4A9EFF` |
| Orange (CTA) | Orange | `#FF7A00` |
| White | White | `#ffffff` |
| Light Gray | Gray | `#f8f9fa` |
| Text Gray | Dark Gray | `#4a5568` |
| Border Gray | Light Gray | `#e2e8f0` |

---

## 🔍 TESTING

### After Applying Theme:

1. **Visual Check:**
   - [ ] Submit button matches website orange
   - [ ] Selected dates are light blue
   - [ ] Text is readable (dark blue)
   - [ ] Inputs have proper borders
   - [ ] Hover states work

2. **Functionality Check:**
   - [ ] Can select date
   - [ ] Can select time
   - [ ] Can fill form fields
   - [ ] Can see submit button
   - [ ] Can click submit button
   - [ ] Booking confirms successfully

3. **Responsive Check:**
   - [ ] Desktop looks good
   - [ ] Tablet looks good
   - [ ] Mobile looks good
   - [ ] Submit button visible on all devices

---

## 🚨 TROUBLESHOOTING

### Submit Button Not Visible

**Solution 1:** Increase iframe height
- Current: 900px desktop, 850px mobile
- Try: 1000px desktop, 950px mobile

**Solution 2:** Enable scrolling
- Already set to `scrolling="yes"`
- User can scroll within iframe

**Solution 3:** Check GHL calendar length
- Long forms need more height
- Reduce optional fields in GHL

### Theme Not Applying

**Reason:** Cross-origin iframe restrictions

**Solution:** Must set theme in GHL dashboard
1. GHL Settings → Calendars
2. Edit your calendar
3. Appearance/Theme section
4. Apply colors there

### Colors Don't Match

**Check:**
1. GHL theme settings saved?
2. Browser cache cleared?
3. Correct calendar URL?
4. URL parameters correct?

---

## 💡 BEST PRACTICES

### For Best User Experience:

1. **Keep form short** - Only essential fields
2. **Use clear labels** - Easy to understand
3. **Match website colors** - Consistent branding
4. **Test on mobile** - Most users book on phone
5. **Ensure button visible** - Critical for conversions

### For Best Appearance:

1. **Use website fonts** - Inter & Sora
2. **Match button style** - Orange gradient
3. **Consistent spacing** - 12px border radius
4. **Proper contrast** - Readable text
5. **Smooth animations** - Professional feel

---

## 📊 EXPECTED RESULT

After proper theme setup:

- ✅ Calendar matches website design
- ✅ Submit button is orange with gradient
- ✅ Selected items are light blue
- ✅ Text is dark blue and readable
- ✅ Inputs have clean borders
- ✅ Hover effects work smoothly
- ✅ Mobile responsive
- ✅ Professional appearance
- ✅ High conversion rate

---

## 🎯 FINAL NOTES

**Current Status:**
- ✅ Iframe height increased to 900px
- ✅ Scrolling enabled
- ✅ Theme URL parameters added
- ✅ Custom CSS injection attempted
- ⚠️ Full theme control requires GHL settings

**Next Steps:**
1. Access GHL calendar settings
2. Apply theme colors listed above
3. Test booking flow
4. Adjust height if needed
5. Monitor conversion rates

**The calendar will look professional and match your website once GHL theme is configured!** 🎨

---

**Last Updated:** May 22, 2026  
**Version:** 5.0 (Theme Optimized)
