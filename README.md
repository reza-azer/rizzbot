# Rizzbot
--feel free to modify intents.json as creative as you would

### 🧠 **Pipeline Utama**
1. **Preprocessing Data**
   - Tokenisasi dan lemmatization dari `intents.json`
   - Membentuk `words`, `classes`, dan `documents`
   - Membuat bag-of-words untuk setiap pattern

2. **Training Preparation**
   - Membentuk `train_x` dan `train_y` sebagai input dan label
   - Shuffle data agar training tidak bias

3. **Model Architecture**
   - Input layer: 128 neuron, ReLU
   - Hidden layer: 64 neuron, ReLU
   - Output layer: jumlah neuron = jumlah intent, Softmax

4. **Training**
   - Optimizer: SGD dengan Nesterov momentum
   - Loss: categorical crossentropy
   - Epochs: 350
   - Batch size: 5

5. **Saving**
   - Model disimpan sebagai `chatbot_model.h5`
   - Vocabulary dan intent disimpan sebagai pickle (`words.pkl`, `classes.pkl`)

