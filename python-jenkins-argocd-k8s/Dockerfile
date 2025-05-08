FROM python:3

# ✅ Step 1: Install required Linux packages (including distutils)
RUN apt-get update && apt-get install -y python3-distutils

# ✅ Step 2: Install Django
RUN pip install django==3.2

# ✅ Step 3: Copy all source files
COPY . .

# ✅ Step 4: Run Django migrations
RUN python manage.py migrate

# ✅ Step 5: Expose port and run server
EXPOSE 8000
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
