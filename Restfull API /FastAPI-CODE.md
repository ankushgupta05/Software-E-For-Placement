Samajh gaya bhai 👍 tum chahte ho **CORS setup** bhi ho jisme React frontend ya koi bhi domain request kar sake (means `*` allow).

Main ekdum **single file with one router + CORS setup** de raha hu 👇

---

## ✅ `main.py`

```python
from fastapi import FastAPI, APIRouter
from fastapi.middleware.cors import CORSMiddleware

# Step 1: FastAPI app
app = FastAPI()

# Step 2: CORS setup (React ya any frontend allow karne ke liye)
app.add_middleware(
    CORSMiddleware,
    allow_origins=["*"],   # "*" means sab allowed (React, Angular, etc.)
    allow_credentials=True,
    allow_methods=["*"],   # GET, POST, PUT, DELETE sab allowed
    allow_headers=["*"],   # all headers allowed
)

# Step 3: Router banaya
router = APIRouter()

# Ek GET route
@router.get("/hello")
def say_hello():
    return {"message": "Hello from Router with CORS enabled!"}

# Step 4: Router ko include kiya
app.include_router(router)

# Extra root route
@app.get("/")
def root():
    return {"message": "FastAPI with single router + CORS is working!"}
```

---

## ✅ Run Command

```bash
uvicorn main:app --reload --port 8000
```

---

### 🔗 Check karo:

* Root → `http://127.0.0.1:8000/`
* Router → `http://127.0.0.1:8000/hello`
* Docs → `http://127.0.0.1:8000/docs`

---

👉 Ab React (ya koi bhi frontend) se easily request jaa sakti hai bina CORS error ke.

Bhai bataun tumhe ek **React fetch example** bhi jisme ye FastAPI API call karte ho?
