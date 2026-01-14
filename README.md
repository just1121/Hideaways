# Coppola Hideaways - Email Templates

Custom HTML email templates for RDP (Resort Data Processing) system.

## Files

| File | Description |
|------|-------------|
| `LL_Confirm_Email.html` | **La Lancha Reservation Confirmation** - Clean, email-safe HTML template |
| `LL_Confirm.doc` | Original Word document |
| `LL_Confirm.doc.html` | Word export (reference only) |
| `images/` | All email images |

## RDP Merge Fields Used

The template uses these RDP merge fields that will be replaced with guest data:

```
[*hreserve.guestname*]       - Guest's full name
[*hreserve.resnum*]          - Reservation confirmation number
[*hreserve.arrivaldate*]     - Check-in date
[*hreserve.departuredate*]   - Check-out date
[*Units.Description*]        - Room type description
[*hreserve.roomrate*]        - Nightly room rate
[*hreserve.depositamount*]   - First deposit amount
[*hreserve.depositamount2*]  - Second deposit amount
[*hreserve.depositduedate2*] - Second deposit due date
```

### Date Format Options
Per RDP documentation, dates can be formatted:
- `[*hreserve.arrivaldate-s*]` → 5/11/2025 (short)
- `[*hreserve.arrivaldate-L*]` → Monday, May 11, 2025 (long)
- `[*hreserve.arrivaldate-dw*]` → Monday (day of week)

## Installation

1. **Update image URLs** in `LL_Confirm_Email.html` to use hosted paths:
   - Replace `images/image1.png` with full URL (e.g., from this GitHub repo or your web server)
   
2. **Copy to RDP server**:
   ```
   <rdp root folder>/Reports10/Confirmations/
   ```

3. **Configure in RDP** to use the new template

## Image Hosting via GitHub

Images can be served directly from this repository using raw URLs:

```
https://raw.githubusercontent.com/just1121/CoppolaHideaways/main/images/image1.png
https://raw.githubusercontent.com/just1121/CoppolaHideaways/main/images/image2.jpg
https://raw.githubusercontent.com/just1121/CoppolaHideaways/main/images/image3.jpg
...etc
```

## Resources

- [RDP HTML Email Documentation](https://secure.irm1.net/irmng/docs/customizationguide/htmlemail.html)
- [The Coppola Hideaways Website](https://www.thecoppolahideaways.com/)

---

*Created January 2026*
