# Ask Rick - Ready to Deploy! 🏌️

## 📦 What's Inside

This folder contains everything you need to deploy "Ask Rick" to Cloudflare Pages.

---

## 📁 File Structure

```
ask-rick/
├── index.html              ← The chat interface
└── functions/
    └── _middleware.js      ← Backend API handler
```

---

## 🚀 How to Deploy

### **Step 1: Go to Cloudflare**
1. Visit: https://dash.cloudflare.com
2. Click **Workers & Pages** (left sidebar)
3. Click **Create application** → **Pages** → **Upload assets**

### **Step 2: Upload This Folder**
1. **Drag and drop this entire folder** (or just the files inside)
2. Click **Deploy site**
3. Wait 1-2 minutes

### **Step 3: Add Your API Key** ⚠️ CRITICAL
1. Go to **Settings** → **Environment variables**
2. Click **Add variable**
3. Fill in:
   - **Variable name:** `OPENAI_API_KEY`
   - **Type:** Secret
   - **Value:** Your OpenAI API key (get it from https://platform.openai.com/api-keys)
   - **Environment:** Production (check the box)
4. Click **Save**

### **Step 4: Redeploy**
1. Go to **Deployments** tab
2. Click **Manage deployment** dropdown
3. Click **Retry deployment** (or **Create deployment**)
4. Wait 30 seconds

### **Step 5: Test!**
1. Visit your site URL (something like `your-project.pages.dev`)
2. Type: **"First tee nerves"**
3. Press Enter
4. Rick should respond! 🎉

---

## ⚠️ Important Notes

- **You MUST add the `OPENAI_API_KEY` environment variable** or it won't work
- The API key should be a **Secret** type (not Text)
- Make sure to select **Production** environment
- After adding the key, you MUST redeploy

---

## 🆘 Troubleshooting

**Still getting HTTP 405 error?**
- Make sure the `functions` folder uploaded correctly
- Check that `_middleware.js` is inside the `functions` folder
- Verify the API key environment variable is set
- Try redeploying again

**API key not working?**
- Verify billing is enabled in your OpenAI account
- Check the key is valid at https://platform.openai.com/api-keys
- Make sure you selected "Secret" type (not "Text")
- Redeploy after adding the key

---

## 💰 Cost

- **Cloudflare Pages:** FREE
- **Cloudflare Workers:** FREE (100,000 requests/day)
- **OpenAI API:** ~$0.005 per conversation

---

## ✅ You're All Set!

Everything is ready to go. Just follow the 5 steps above and you'll be live in minutes!

**Questions? Issues? Check the deployment details in your Cloudflare dashboard.**

Good luck! 🏌️⛳
