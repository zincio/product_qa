Product Q&A
-----------
Use [Zinc Product Data API](https://zincapi.com/) and [OpenAI GPT-3](https://openai.com/) to answer questions about an Amazon product.

Usage
-----
```bash
# OpenAI key is always required
export OPENAI_API_KEY=sk-YourOpenAiKey

# Zinc key can be omitted for some example products, but is required otherwise
export ZINC_CT=your-zinc-ct

# Summarize a product
./product-qa B01EOY7LTA

# Ask a specific question
./product-qa B01EOY7LTA --question "What is the size of the bit?"
```

Installation
------------
```bash
virtualenv -p python3 venv
source ./venv/bin/activate
pip install -r requirements.txt
```

Or even simpler:
```bash
pip install openai faiss-cpu langchain
```

Example result
--------------
```
$ ./product-qa B01EOY7LTA
Categories ['Hand Tools', 'Screwdrivers & Nut Drivers', 'Tools & Home Improvement', 'Screwdrivers']
Durability
         Klein Tools electronics screwdrivers are designed for precision work, and feature a swivel cap for optimum control. Made of the highest quality tempered steel, carefully heat-treated for maximum strength, and precision milled to fit screw openings securely. Rotating caps and Klein's exclusive Cushion-Grip handles offer outstanding comfort and control. Corrosion-resistant chrome plated barrel that includes two double-ended bits that exceed ANSI standards.

Quality
         Great! Can't beat Klein!

Price
         $10.97

Ergonomics
         Cushion-Grip handles for maximum comfort when working on small equipment.

Versatility
         This product is versatile as it offers 2 Phillips and 2 slotted choices, which are great for small appliances and electronics, and it has interchangeable shaft for quick bit switch out. It is also corrosion-resistant and has a rotating cap for optimum and precise control.

Performance
         This product is designed for precision work and features a swivel cap for optimum control. It is made of the highest quality tempered steel, carefully heat-treated for maximum strength, and precision milled to fit screw openings securely. Rotating caps and Klein's exclusive Cushion-Grip handles offer outstanding comfort and control. Corrosion-resistant chrome plated barrel that includes two double-ended bits that exceed ANSI standards.

You would buy this product because it offers 2 Phillips and 2 slotted choices, is well made and has a rotating cap for optimum and precise control. It is also made of the highest quality tempered steel, carefully heat-treated for maximum strength, and precision milled to fit screw openings securely. It also has Klein's exclusive Cushion-Grip handles for outstanding comfort and control.
```

```
$ ./product-qa B095BZT4SD --question "can it be used as a stand?"
Yes, the Samsung Tab A7 Lite Case has flip capability to transform the case into a viewing stand and keyboard stand.
```
