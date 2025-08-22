# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## Expanding the ESLint configuration

If you are developing a production application, we recommend using TypeScript with type-aware lint rules enabled. Check out the [TS template](https://github.com/vitejs/vite/tree/main/packages/create-vite/template-react-ts) for information on how to integrate TypeScript and [`typescript-eslint`](https://typescript-eslint.io) in your project.

# 🖼️ React Image Enhancer

A **React-based web app** that allows users to **upload and enhance images** using an external API.  
This project integrates with the **TechHK image enhancement API** to upscale and process images seamlessly.  

---

## 🛠️ Tech Stack
- **Frontend:** React (CRA / Vite)  
- **API Calls:** Axios + Fetch  
- **Styling:** CSS / Tailwind (if used)  
- **External API:** [TechHK Image Enhancement API](https://techhk.aoscdn.com/)  

---

## 🚀 Features
✔️ Upload an image from your computer  
✔️ Send it to the **enhancement API**  
✔️ Poll the API until the enhanced version is ready  
✔️ Display the enhanced image in the app  
✔️ Error handling (upload failures, retries, API errors)  

## 🔄 API Workflow

The app integrates with the **TechHK Image Enhancement API** to process images.  
Here’s how the workflow happens step by step:

1. **Upload Image**
   - User selects an image.
   - The app sends a `POST` request with the image file to:
     ```http
     POST https://techhk.aoscdn.com/api/tasks/visual/scale
     ```
   - Response includes a unique `task_id`.

   Example Response:
   ```json
   {
     "status": 200,
     "message": "success",
     "data": {
       "task_id": "187b1adc-b35f-46d7-8670-47f88f89fd73"
     }
   }
