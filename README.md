# 🎮 Canyon Battlefield - Team Assignment Generator

A web-based platform for generating strategic team assignments for **Canyon Battlefield** game mode. Upload your player data, get optimized team assignments with visual infographics.

---

## 🚀 **Quick Start**

### **Option 1: Local Use (Recommended)**
1. Download `canyon_storm_generator.html`
2. Open the HTML file in your browser (Chrome, Firefox, Safari, Edge)
3. Follow the on-screen instructions

### **Option 2: GitHub Pages Hosting**
1. Create a GitHub repository
2. Upload the HTML file and rename it to `index.html`
3. Enable GitHub Pages in Settings → Pages
4. Share the URL with your team

**No installation, no server, no dependencies required!** ✨

---

## 📋 **How to Use**

### **Step 1: Prepare Your Data**
1. Click **"Download Excel Template"** in the HTML
2. Open the Excel template
3. Fill in player information:
   - **Column B:** Player Name
   - **Column D:** E1 troops (Tank, Aero, or Missile)
   - **Column E:** E1 total power (e.g., 65.0)
   - **Column F:** Canon Battlefield - Team A (1 = selected)
   - **Column G:** Canon Battlefield - Team B (1 = selected)

**Template Structure:**
```
Row 1-9: Instructions
Row 10: Headers (Player Name, E1 troops, Canon Battlefield - Team A, etc.)
Row 11+: Player data
```

### **Step 2: Upload**
1. Save your Excel file
2. Click **"📤 Upload Your File"** in the HTML
3. System processes and assigns players automatically

### **Step 3: Download Outputs**
1. Click **"Download Excel"** → Get Excel with assignments
2. Click **"Download Team A Image"** → Get Team A infographic (PNG)
3. Click **"Download Team B Image"** → Get Team B infographic (PNG)

**Output:** 3 files showing player assignments by zone and priority

---

## 🎯 **Smart Assignment Strategy**

### **Priority-Based Assignment**
- **P1 (Highest):** Middle Power Tower, Virus Lab → Strongest players (68M, 65M, 64M...)
- **P2:** Middle Power Tower → Very strong players (62M, 60M...)
- **P3:** East/West Serum Factories, Defense Systems → Strong players (59M, 58M, 57M...)
- **P4:** North Data Centers → Good players (56M, 55M...)
- **P5:** East/West/North Roaming → Decent players (54M, 53M...)
- **P6 (Lower):** South Samples → Balanced players (52M, 51M, 50M...)

### **Troop Type Mixing**
The algorithm automatically mixes troop types for tactical advantage:
- **Tank + Aero** → Balanced composition ✓
- **Tank + Missile** → Balanced composition ✓
- **Aero + Missile** → Balanced composition ✓

Avoids pairing same types (Tank + Tank, Aero + Aero, Missile + Missile)

### **Power Balancing**
Even lower priority buildings (P6) get capable players (~50M), not weak leftovers. This ensures every zone has effective defenders.

**Example Assignment:**
```
P1: Middle Power Tower
  → Player1 (68M, Aero)
  → Player2 (65M, Tank) ✓ Mixed troops

P3: East Serum Factory 2
  → Player5 (57M, Aero) ← Still strong

P6: South Sample 1
  → Player15 (50M, Missile) ← Balanced
```

---

## 📊 **Canyon Battlefield Buildings**

```
Priority 1: Middle Power Tower (3 slots), Middle Virus Lab (4 slots)
Priority 2: Middle Power Tower (1 slot)
Priority 3: East/West Serum Factories, Defense Systems (1 slot each)
Priority 4: North Data Centers 1-2 (1 slot each)
Priority 5: East/West/North Roaming (1 slot each)
Priority 6: South Samples 1-4 (1 slot each)

Total: 20 players per team
```

**Zone Organization:**
- **EAST Zone:** Serum Factory 2, Defense System 2, Roaming
- **SOUTH Zone:** Sample Warehouses 1-4 (capture objectives)
- **WEST Zone:** Serum Factory 2, Defense System 2, Roaming
- **NORTH Zone:** Data Centers 1-2, Roaming
- **MIDDLE Zone:** Power Tower (3 slots), Virus Lab (4 slots)

---

## ✅ **Features**

- ✅ **No Installation:** Pure HTML/JavaScript, works in any browser
- ✅ **Offline Capable:** No internet needed after initial load
- ✅ **Excel Integration:** Upload/download Excel files
- ✅ **Checkbox Support:** Accepts 1, true, 'Y', or 'TRUE' as selections
- ✅ **Table Infographics:** Clean, professional table layout
- ✅ **Zone Organization:** Buildings grouped by battlefield zone
- ✅ **Priority Colors:** Visual priority coding
- ✅ **Smart Assignment:** Troop type mixing + power balancing
- ✅ **Triple Output:** Excel + 2 PNG infographics
- ✅ **Error Validation:** Checks for missing players, wrong formats
- ✅ **Console Debugging:** See detailed assignment logs
- ✅ **Mobile Friendly:** Works on phones and tablets

---

## 🔧 **Technical Details**

### **Technologies Used:**
- **HTML5** - Structure
- **CSS3** - Styling and animations
- **JavaScript (ES6+)** - Logic and processing
- **SheetJS (XLSX.js)** - Excel file handling
- **Canvas API** - Image generation

### **Browser Compatibility:**
- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+
- ✅ Mobile browsers (iOS Safari, Chrome Mobile)

### **File Sizes:**
- `canyon_storm_generator.html`: ~36 KB
- Generated PNGs: ~100-500 KB each
- Excel outputs: ~8-15 KB

### **Performance:**
- Excel processing: < 1 second
- Image generation: < 2 seconds
- Works with 100+ player lists

---

## 🐛 **Troubleshooting**

### **"NO PLAYERS!" Error**
**Problem:** No players marked in Excel  
**Solution:** Make sure you put `1` in column F (Team A) or G (Team B) for each player

### **"Excel file must contain..." Error**
**Problem:** Sheet names don't match  
**Solution:** Sheets must be named "Players", "Canyon Battlefield - Team A", "Canyon Battlefield - Team B"

### **Infographic Won't Download**
**Problem:** Browser blocking download  
**Solution:** 
1. Check browser console (F12) for errors
2. Make sure pop-ups are allowed
3. Try a different browser

### **Building Names Missing in Excel**
**Problem:** Reading from wrong Excel row  
**Solution:** This should be fixed in the latest version. Make sure you downloaded the updated HTML.

### **Template Downloads Empty File**
**Problem:** Browser security settings  
**Solution:** Allow downloads from local HTML files, or host on GitHub Pages

---

## 📖 **Excel Template Guide**

### **Required Columns:**

#### **Players Sheet:**
| Column | Name | Description | Example |
|--------|------|-------------|---------|
| A | Row Number | Sequential number | 1, 2, 3... |
| B | Player Name | Player's in-game name | "Sw3k" |
| C | Total Hero Power(M) | Optional | 95 |
| D | E1 troops | Tank, Aero, or Missile | "Tank" |
| E | E1 total power(M) | Player's E1 power | 65.0 |
| F | Canon Battlefield - Team A | 1 = selected, 0 = not | 1 |
| G | Canon Battlefield - Team B | 1 = selected, 0 = not | 0 |

#### **Building Sheets (Team A & Team B):**
| Column | Name | Description |
|--------|------|-------------|
| A | Buildig Name | Building name (exact match) |
| B | Priority | Building priority (1-6) |
| C | Names | Leave empty (auto-filled) |
| D | Description | Building instructions |

### **Important Notes:**
- ✅ Headers must be exact (including typo "Buildig")
- ✅ Use `1` for selected players (not "X" or "Yes")
- ✅ E1 power must be numeric (65.0, not "65M")
- ✅ Troop type must be: Tank, Aero, or Missile (exact spelling)

---

## 🎨 **Customization**

### **Modify Building Priorities**
Edit the building sheet in Excel template:
```
Building Name         | Priority | Description
--------------------- | -------- | -----------
Middle Virus Lab      | 1        | Critical objective
East Serum Factory 2  | 3        | Secondary objective
South Sample 1        | 6        | Capture zone
```

Change priorities to adjust assignment order.

---

## 📱 **Mobile Usage**

### **On Mobile Devices:**
1. ✅ Open HTML in mobile browser (Safari, Chrome)
2. ✅ Upload Excel from cloud storage (Google Drive, Dropbox)
3. ✅ Download outputs to phone
4. ✅ Share images via WhatsApp, Discord, Telegram

---

## 🔐 **Privacy & Security**

- ✅ **100% Local Processing:** All data stays in your browser
- ✅ **No Server:** No data sent to any server
- ✅ **No Tracking:** No analytics or cookies
- ✅ **No Account:** No registration required
- ✅ **Offline Capable:** Works without internet

**Your player data never leaves your device!**

---

## 📚 **Additional Resources**

### **Documentation Files:**
- `CANYON_ASSIGNMENT_STRATEGY.md` - Detailed assignment algorithm
- `CANYON_FIXES.md` - Bug fixes and solutions
- `CANYON_ORDER_FIX.md` - Building order explanation

---

## 🤝 **Support**

### **Having Issues?**
1. Check the troubleshooting section above
2. Open browser console (F12) to see detailed logs
3. Verify Excel template format matches examples
4. Try in a different browser

### **Feature Requests?**
This is a standalone HTML tool. For customization:
1. Edit the HTML file directly (HTML/CSS/JavaScript knowledge required)
2. Or request changes from your system administrator

---

## 📄 **Version History**

### **Canyon Battlefield:**
- **v3.0** - Smart assignment algorithm with troop mixing
- **v2.0** - Building order fixes, infographic downloads
- **v1.0** - Initial release with Excel integration

---

## ⚡ **Performance Tips**

1. **Use latest browser version** for best performance
2. **Close unnecessary tabs** when generating large assignments
3. **Clear browser cache** if experiencing issues

---

## 🎯 **Best Practices**

### **For Organizers:**
1. **Test with sample data** before using real player lists
2. **Keep backup** of original Excel files
3. **Share templates** with team members early
4. **Verify assignments** before battle day
5. **Download all outputs** before closing browser

### **For Players:**
1. **Fill Excel accurately** (power, troop type)
2. **Mark availability** clearly (1 or 0)
3. **Update power levels** before each battle
4. **Check assignments** in infographics

---

## 📞 **Credits**

Developed for competitive Last War: Survival Canyon Battlefield coordination.

**Built with:** HTML5, JavaScript, Canvas API, SheetJS

**Designed for:** UBS Alliance and competitive Last War: Survival players worldwide

---

## 🚀 **Getting Started Checklist**

- [ ] Download `canyon_storm_generator.html`
- [ ] Open in browser to verify it works
- [ ] Download Excel template
- [ ] Fill template with 3-5 test players
- [ ] Upload and verify outputs
- [ ] Collect real player data
- [ ] Generate final assignments
- [ ] Share infographics with team
- [ ] Battle! 🎮

---

## 🎮 **Ready to Battle?**

1. Download the HTML generator
2. Prepare your player data
3. Generate assignments
4. Share with your team
5. Dominate Canyon Battlefield! 🏆

---

**Made with ❤️ for competitive Last War: Survival players**

*Last Updated: February 2026*
