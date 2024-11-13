
# Tender Information Extractor

This project reads a PDF document containing tender information and extracts specific details, saving them in a structured JSON format for easy access and analysis. This project focuses on extracting important tender-related information such as the timeline, financial requirements, eligibility criteria, and contact information.

## Project Overview

The goal of this project is to parse tender documents and extract relevant information automatically. The extracted data includes:

- **Tender Overview**: Reference number, title, and institution.
- **Timeline**: Important dates for bid submissions and openings.
- **Financial Requirements**: Fees, EMD (Earnest Money Deposit), and payment terms.
- **Eligibility Criteria**: Exemptions, required documentation, and other criteria.
- **Technical Specifications**: Description and quantity of items required.
- **Fees & Payments**: Submission method, payment account details, and address.
- **Contact Information**: Address, email, and phone for tender-related inquiries.
- **Tender Evaluation**: Stages and criteria for evaluation.
- **Additional Information**: Local supplier requirements and DPIIT compliance.

## Sample Output

The output JSON format is as follows:

```json
{
    "tender_overview": {
        "reference_number": "e-Tender Notice - NITJ/DRC/PUR/TT/36/2024",
        "title": "Fabrication of Machine for Continuous Production of Textile Waste Based Composite Materials",
        "institution": "Dr. B.R. Ambedkar National Institute of Technology (NIT), Jalandhar"
    },
    "timeline": {
        "start_date": "2024-10-16T15:00:00",
        "last_date_submission_online": "2024-11-06T15:00:00",
        "physical_submission_fee_emd": "2024-11-07T15:00:00",
        "technical_bid_opening": "2024-11-07T15:00:00"
    },
    "financial_requirements": {
        "tender_fee": "500 INR (Non-Refundable)",
        "emd": "90000 INR (Refundable)",
        "payment_terms": "Demand Draft"
    },
    ...
}
```

## Installation

### Prerequisites

- Python 3.x
- PDF processing libraries (`pdfplumber`, `PyMuPDF`)

Install the necessary libraries:

```bash
pip install pdfplumber PyMuPDF
```

## Usage

1. Clone the repository:

    ```bash
    git clone https://github.com/your-username/tender-info-extractor.git
    cd tender-info-extractor
    ```

2. Run the extraction script with your PDF document:

    ```bash
    python main.py /path/to/tender-document.pdf
    ```

3. The script will output a JSON file (`tender_info.json`) with the extracted data.

## Configuration

Modify `main.py` to adjust extraction settings or to include additional fields if needed.

