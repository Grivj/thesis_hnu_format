# 噪声辅助对抗性例子检测：一种简单有效的识别恶意输入的方法: Noise-Aided Adversarial Example Detection: A Simple and Effective Method for Identifying Malicious Inputs

This thesis explores the robustness of deep neural networks (DNNs) when subjected to adversarial examples—carefully crafted inputs designed to deceive models into incorrect predictions. With the growing deployment of DNNs in applications ranging from self-driving cars to image and speech recognition, understanding and mitigating these vulnerabilities has become crucial.

## Viewing the Full Thesis

For a detailed analysis and further results, [click here to view the full thesis PDF](main.pdf).


## Motivation

Deep neural networks have excelled in various tasks, including:
- Image and speech recognition [Russakovsky et al., 2015; Amodei et al., 2015]
- Autonomous driving [Bojarski et al., 2016]
- Playing complex games like Go [Silver et al., 2016]

However, DNNs are vulnerable to adversarial examples—small, often imperceptible perturbations in input data that lead to misclassifications. Below is an example:
![misclassifications example](https://github.com/user-attachments/assets/b2e62cec-6b73-4686-ab8c-773cd428fc8f)

Additionally, the difference in robustness between random noise and adversarial noise motivated me to explore the stability of adversarial examples under added random perturbations.

## Main Contribution

In this thesis, I propose a novel method to detect adversarial examples by introducing Gaussian noise of varying intensity to the inputs and evaluating the model's prediction consistency. This method:
- Does not require prior knowledge about the type of adversarial attack.
- Is computationally efficient, requiring no parameter training or optimization.
- Can be combined with other detection techniques for enhanced efficacy.

This approach emerged after analyzing the effects of Gaussian noise on both normal and adversarial images, revealing significant disparities not discussed in prior work.

本研究的主要贡献在于提供了一种简单、高效且可扩展的对抗样本检测方法，以应对深
度学习模型在实际应用中所面临的安全挑战。通过实验证明了该方法的有效性，并与现
有方法进行了比较分析，为后续研究提供了宝贵的参考。

在本研究中，我们成功地提出了一种简单、高效且可扩展的对抗样本检测方法。然而，
我们认识到这项研究仍有一些局限性和未来的改进方向。

- 深入分析不同类型的对抗性攻击：虽然本研究涉及了一些常见的对抗性攻击方法，但未来的研究可以考虑探索更多的攻击策略，以便更全面地评估所提方法的鲁棒性。
- 扩展到其他任务和领域：本研究主要关注图像分类任务，但对抗性攻击同样存在于其他计算机视觉任务，如目标检测、语义分割等。未来的研究可以将所提方法应用于这些任务，以验证其在不同场景下的有效性。
- 研究更多的防御策略：除了本文提出的对抗样本检测方法外，还可以研究其他防御策略，如对抗性训练、模型蒸馏和特征空间变换等。这将有助于构建一个更强大、更全面的防御体系，进一步提高模型的鲁棒性。
- 模型可解释性与安全性：为了增强对抗性攻击的防御能力，可以研究提高模型的可解释性，从而更好地理解其在面对对抗性样本时的行为。通过提高模型的可解释性，我们可以揭示模型的薄弱环节，进而设计出更强大的防御策略。
