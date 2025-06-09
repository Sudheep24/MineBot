# MineBot — AI-Powered Legal Assistant

MineBot provides **free legal information** and helps businesses save **10-15% on compliance costs** by automating legal FAQs. It offers mobile and web access, making legal support efficient and accessible.

**Key Features:**
- Custom AI chatbot tailored to your legal needs
- Multilingual support for diverse users
- Automated FAQs for fast, reliable answers

---

## 🚀 Built With

<p align="left">
  <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white" />
  <img src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=next.js&logoColor=white" />
  <img src="https://img.shields.io/badge/Tailwind_CSS-38bdf8?style=for-the-badge&logo=tailwind-css&logoColor=white" />
  <img src="https://img.shields.io/badge/Pinecone-4285F4?style=for-the-badge&logo=google-cloud&logoColor=white" />
  <img src="https://img.shields.io/badge/Vercel_AI_SDK-000000?style=for-the-badge&logo=vercel&logoColor=white" />
  <img src="https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white" />
</p>

---

## 📁 Project Structure

This project uses a simple client/server architecture separating the frontend and backend for easy stack swapping.

### Frontend Client

- Built with Next.js, Tailwind CSS, and Vercel AI SDK components to deliver the chatbot experience.  
- Uses API routes to interact with the backend for document context retrieval.  
- Stores workspace data locally for a seamless user experience.

### Backend Server

- Built with Node.js and Express.  
- Handles file uploads, validation, chunking, embedding, and upserting to Pinecone.  
- Manages document namespaces for multi-tenant support.

---

## 🧠 Core Concepts

### Multi-Tenant RAG Architecture

- Uses Pinecone namespaces to isolate tenant data.  
- Documents are chunked into paragraphs and embedded for semantic search.  
- Embeddings are upserted with metadata including reference URLs.  
- Document and workspace deletions are supported by chunk ID prefixing and namespace cleanup.

---

## 🔧 How It Works

1. **File Upload & Chunking:** PDFs are parsed and split into paragraph-sized chunks.  
2. **Embedding:** Chunks are embedded using OpenAI’s text-embedding-3-small model.  
3. **Upsertion:** Embeddings are upserted to Pinecone in tenant-specific namespaces.  
4. **Retrieval & Prompt Creation:** When a user queries, the system fetches top relevant chunks from Pinecone and builds a prompt that the AI chatbot uses to generate accurate, context-aware responses.  
5. **Document & Workspace Management:** Supports targeted chunk deletions for documents and full namespace deletes for workspace offboarding.

---

## 📦 Usage

- Upload your legal documents or FAQs to create a knowledge base.  
- Interact with MineBot to get fast, accurate legal answers.  
- Manage multiple tenants or workspaces seamlessly with isolated namespaces.

---

## 📸 Screenshots / Images

<!-- Replace these with actual image links after uploading to your repo or an image hosting platform -->

![Frontend Chat Interface](ss1)

![Backend Architecture](ss2)

![Pinecone Namespace](ss3)

---

Feel free to customize and extend this README with installation instructions, environment setup, or API usage examples as needed!
