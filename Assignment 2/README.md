# 1. Entity Relationship Diagram (ERD) For HRMS  
<img width="433" alt="image" src="https://github.com/user-attachments/assets/d2f2c4d2-c3aa-49d5-9543-f6225566a99d" />    

# 2. API in Python Using FastAPI  


# 3. Pydantic Models
#Pydantic Model
from pydantic import BaseModel
from typing import List, Optional
from datetime import date

# Candidate Model
class Applicant (BaseModel):
    first_name: str
    last_name: str
    phone: str
    email: str
    date_applied: date
    experience: int
    status: str

# Job Model
class Job(BaseModel):
    title: str
    location: str
    department: str
    salary: str
    status: str
    posting_date: date
    closing_date: date

# Application Model
class Application(BaseModel):
    applicant_id: str
    job_id: str
    application_date: date
    status: str

# Recruiter Model
class Recruiter(BaseModel):
    first_name: str
    last_name: str
    email: str
    phone: str
    department: str

# Interview Model
class Interview(BaseModel):
    applicant_id: str
    recruiter_id: str
    interview_date: date
    interview_time: str
    interview_status: str

# Offer Model
class Offer(BaseModel):
    application_id: str
    salary_offered: str
    offer_date: date
    status: str

# Company Model
class Company(BaseModel):
    company_name: str
    location: str
    industry: str
