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
$ ./product-qa B095BZT4SD                                                                                ret:0 
Categories ['Tablet Accessories', 'Tablet Cases', 'Bags, Cases & Sleeves', 'Cases']
Durability 
	 Great durability, sturdiness and easy to hold. 

Protection 
	 Durable protective hardback with premium quality PU leather. Soft scratch-free microfiber interior adds comfort and an additional layer of protection. 

Style 
	 Case 

Price 
	 $11.99 

Compatibility 
	 This case is compatible with Samsung Galaxy Tab A7 Lite 8.7 inch Model (SM-T220/T225/T227) 2021 Release. It will NOT work for any other model device. 

Quality 
	 Reviews indicate that this product is of good quality, providing protection for the Samsung tablet and is lightweight and not bulky. 

You would buy this product because it is a slim and lightweight hard back design that adds minimal bulk while offering your device great protection. It has a trifold stand, durable protective hardback with premium quality PU leather, soft scratch-free microfiber interior, precise cutouts for easy access to all the controls and features, and is compatible with the Samsung Galaxy Tab A7 Lite 8.7 inch Model (SM-T220/T225/T227) 2021 Release.
```

```
$ ./product-qa B095BZT4SD --question "can it be used as a stand?"
Yes, the Samsung Tab A7 Lite Case has flip capability to transform the case into a viewing stand and keyboard stand.
```
