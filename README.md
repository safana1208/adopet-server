# AdoPet Admin Panel

The **AdoPet Admin Panel** is the administration interface for the AdoPet pet adoption system. It allows staff to manage pets, adoption requests, statistics, and view detailed pet profiles.

## Features

✅ View and manage all pets in the system  
✅ Add new pets (including image upload)  
✅ Edit and delete pet information  
✅ View adoption requests with status management (Approve/Decline)  
✅ View system statistics (adoptions, users, donations, etc.)  
✅ Pet profile viewer with description and link  
✅ Admin-only access with login authentication

## Technologies Used

- HTML, CSS, JavaScript (Vanilla)
- Fetch API for communication with backend (hosted on Render)
- Cloudinary (optional) for image hosting
- Responsive design for admin control on desktop

## File Structure

```
admin-dashboard.html       # Main dashboard showing all pets
admin-pet-profile.html     # Detailed pet view and edit option
admin-requests.html        # Adoption request management
admin-stats.html           # Dashboard with statistics and graphs
assets/                    # Admin images and icons
css/style.css              # Shared styles
js/                        # Admin-specific JS logic
```

## Deployment

- The admin panel is part of the client-side repo, but accessible only to admin users after login.
- Admin login is identified via phone number and password from the database.
- All data interactions are made via API requests to the [Render-hosted backend](https://adopet-server.onrender.com).

## Notes

- Admin access is restricted and validated via login.
- Adoption requests update both pet status and request status.
- Statistics are fetched dynamically from MongoDB via Express backend.

## Example Admin Flow

1. Admin logs in via login.html (with phone/password)
2. Redirected to `admin-dashboard.html`
3. Views, adds, edits, or deletes pets
4. Navigates to `admin-requests.html` to manage adoption requests
5. Reviews platform data via `admin-stats.html`

---

🔒 **For internal use only – not intended for public adoption users.**
