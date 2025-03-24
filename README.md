# E-commerce Recommendation System

An advanced product recommendation engine for e-commerce platforms that combines multiple recommendation strategies, natural language processing, computer vision, and A/B testing to provide highly personalized product suggestions through various interaction methods.

## Features

### Core Recommendation System
- **Hybrid Recommendation System**: Combines three powerful recommendation approaches:
  - Content-Based Filtering
  - Collaborative Filtering
  - Neural Collaborative Filtering (Deep Learning)

- **Ensemble Methodology**: Weighted combination of multiple recommendation techniques with configurable weights

- **User Activity Tracking**: Captures views, searches, and purchases with temporal weighting

- **User Profiles**: Authentication system with personalized recommendations based on activity history

### Advanced Search Capabilities
- **Natural Language Search**: Understand complex queries like "comfortable running shoes for winter" using semantic meaning
  
- **Image-Based Search**: Find visually similar products by uploading product images using deep learning

- **Multimodal Search**: Combine image and text for refined search (e.g., "this dress but in blue")

- **AI Shopping Assistant**: Conversational interface that understands shopping requests and provides personalized recommendations

### A/B Testing & Optimization
- **A/B Testing Framework**: Create and manage experiments with different recommendation strategies
  
- **Statistical Analysis**: Measure the performance of different variants with significance testing

- **Automated Optimization**: Apply the best-performing variant based on key metrics

### User Interface & Visualization
- **Admin Dashboard**: Monitor system performance, test management, and recommendation weight adjustment

- **Recommendation Visualization**: Clear explanation of how each recommendation method works

- **Feedback System**: Collect and analyze user ratings on recommendations

## Technical Implementation

### Recommendation Models
- **Content-Based Filtering**: TF-IDF vectorization and cosine similarity to find related products
  
- **Collaborative Filtering**: User-item interaction analysis with SVD dimensionality reduction
  
- **Neural Collaborative Filtering**: Deep learning with user and item embeddings for complex pattern recognition

### Natural Language Processing
- **Semantic Search**: SentenceTransformer models for meaning-based product search
  
- **Entity Extraction**: Identify attributes like colors, brands, and price ranges from natural language
  
- **Intent Classification**: Understand user search intent for more relevant results

### Computer Vision
- **MobileNetV2**: Pre-trained CNN for extracting visual features from product images
  
- **Visual Similarity**: Find products with similar visual characteristics using feature vector comparison
  
- **Image Enhancement**: Preprocessing techniques to improve feature extraction quality

### A/B Testing Infrastructure
- **Variant Management**: Create and manage different recommendation configurations
  
- **Random Assignment**: Statistical sampling for unbiased user assignment
  
- **Performance Metrics**: Track clicks, conversions, and ratings for each variant
  
- **Statistical Significance**: Calculate confidence levels and lift metrics

### Tech Stack
- **Backend**: Flask (Python)
- **Database**: SQLite with SQLAlchemy ORM
- **Machine Learning**: TF-IDF, SVD, SentenceTransformers, spaCy
- **Deep Learning**: TensorFlow/Keras for Neural Networks and Computer Vision
- **Frontend**: HTML, CSS, JavaScript, Bootstrap

## Installation

1. Clone the repository
```bash
cd ecommerce-recommendation-system
```

2. Create and activate a virtual environment
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies
```bash
pip install -r requirements.txt
```

4. Install additional NLP components
```bash
python -m spacy download en_core_web_sm
```

5. Initialize the database
```bash
flask db init
flask db migrate
flask db upgrade
```

6. Run the application
```bash
flask run
```

## Usage

### User Features
- **Personalized Recommendations**: Receive customized product suggestions based on browsing history
- **Multiple Search Options**: Use text, natural language, image upload, or conversation-based search
- **AI Assistant**: Chat with the AI assistant for natural language product discovery
- **Feedback**: Rate recommendations to improve future suggestions

### Admin Features
- **Dashboard**: View analytics on system performance and user engagement
- **Weight Adjustment**: Modify the influence of different recommendation models
- **A/B Testing**: Create and monitor tests for optimizing recommendation strategies
- **Performance Metrics**: Track click-through rates, conversion rates, and user ratings


## How It Works

### Hybrid Recommendation System
The system combines three approaches with configurable weights:

1. **Content-Based Filtering**: Uses TF-IDF vectorization and cosine similarity to find products with similar features to those a user has interacted with.

2. **Collaborative Filtering**: Recommends products based on what similar users have liked, using patterns in user behavior with temporal decay.

3. **Neural Collaborative Filtering**: Uses deep learning with embedding layers to model complex user-item interactions for discovering non-linear patterns.

### Natural Language Search
The system processes natural language queries through:
1. Entity extraction to identify product attributes (color, price, brand)
2. Semantic embedding using SentenceTransformers
3. Attribute-based filtering and similarity scoring

### Image-Based Search
When a user uploads an image:
1. MobileNetV2 extracts a 1280-dimensional feature vector
2. The system compares this vector with pre-computed vectors for all products
3. Products with the highest cosine similarity are returned

### A/B Testing Framework
The A/B testing system:
1. Creates variants with different recommendation weights
2. Randomly assigns users to variants
3. Tracks performance metrics (CTR, conversion rate, ratings)
4. Calculates statistical significance and lift
5. Can automatically apply the best-performing configuration

## Future Improvements

- **Reinforcement Learning**: Optimize recommendations based on long-term user satisfaction
- **Enhanced NLP**: Implement more advanced models (BERT, GPT) for complex query understanding
- **More Advanced CV**: Product segmentation and attribute extraction from images
- **Time-Aware Recommendations**: Capture seasonal trends and preference evolution
- **Explainable AI**: More detailed explanation of why products are recommended

## License

[MIT License](LICENSE)

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## Contact

Aayush Sharma