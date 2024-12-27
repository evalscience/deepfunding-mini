# DeepFunding Mini-Contest 🚀

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]()

DeepFunding Mini is a [mini-contest](https://huggingface.co/spaces/DeepFunding/PredictiveFundingChallengeforOpenSourceDependencies) to create a distilled human judgment mechanism predicting the amount of past funding received by open source projects.

## 📦 Data

The mini dataset represents pairs of GitHub repositories taken from the [Ethereum dependency graph](https://github.com/deepfunding/dependency-graph) and their funding amounts in historical funding rounds data. 

- **Training Data:** 3,410 comparisons between 245 repos, 2,387 provided for training
- **Test Data:** 1,023 predictions on the relative funding received between any 2 projects, which get tested against actual data

**Dataset:** [evalscience/deepfunding-mini](https://huggingface.co/datasets/evalscience/deepfunding-mini)

## 🎯 Goal 

Predict the relative funding received between pairs of projects. Each comparison should output a relative value between repositories that sums to 1.

## 🏆 Prizes

Winners receive up to $20,000 based on:
- Novelty and approach in predicting 1,023 comparisons  
- Infrastructure and datasets created

**Evaluation Metric:** Mean Squared Error (MSE) - lower is better, but avoid overfitting.

**Important:** Submission weights must maintain transitivity:
- For any triple _a_, _b_, _c_: `c/a = c/b * b/a`
- Example: If A gets twice as much as B, and B gets three times as much as C, then A must be six times better than C

## 📈 Current Baseline Results

| Metric  | MSE |
|---------|-----|
| Random  | 0.12502730425363476 |
| Stars   | 0.19531555755620916 |
| Forks   | 0.1874321641202411  |
| Funding | 0.08316942192812525 |

## 🏛 Learn More with Eval.Science

Join us at [Eval.Science](https://eval.science) to become part of the next generation of decentralized data scientists tackling important problems like DeepFunding.

## 🔗 Quick Links

- [🎥 YouTube Channel](https://www.youtube.com/@evalscience)
- [📚 Lecture Notes (WIP)](https://docs.eval.science)
- [🤗 Hugging Face Space](https://huggingface.co/spaces/DeepFunding/PredictiveFundingChallengeforOpenSourceDependencies)
- [📊 GitHub Dependency Graph](https://github.com/deepfunding/dependency-graph)
- [💻 Eval.Science Website](https://eval.science)

## 🛠️ Getting Started

1. Click the "Open in Colab" button above
2. Make a copy of the notebook
3. Run all cells
4. Start experimenting!

## 📝 Citation

If you use this dataset in your research, please cite:

```bibtex
@misc{deepfunding2024,
  title={DeepFunding Mini Dataset: Predictive Funding Challenge for Open Source Dependencies},
  author={DeepFunding.org, Eval.Science},
  year={2024},
  publisher={Hugging Face},
  howpublished={\url{https://huggingface.co/datasets/evalscience/deepfunding-mini}}
}
```

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
