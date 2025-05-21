{
  "model": "CATRNN",
  "version": "2.0",
  "context_size": 65000,
  "architecture": {
    "type": "recurrent",
    "layers": [
      {
        "type": "embedding",
        "vocab_size": 100000,
        "dimension": 512
      },
      {
        "type": "lstm",
        "units": 1024,
        "dropout": 0.2
      },
      {
        "type": "lstm",
        "units": 1024,
        "dropout": 0.2
      },
      {
        "type": "dense",
        "units": 100000,
        "activation": "softmax"
      }
    ]
  },
  "training": {
    "optimizer": "adam",
    "learning_rate": 0.001,
    "epochs": 50,
    "batch_size": 32
  },
  "purpose": "multi-token prompt story generation"
}
