---
title: "Generative Adversarial Networks (GANs)"
date: 2025-08-25
summary: "An introduction to GANs, their architecture, and applications."
hideSummary: false
---

## What are GANs?

Generative Adversarial Networks (GANs) are a class of machine learning frameworks introduced by Ian Goodfellow in 2014. GANs consist of two neural networks, the generator and the discriminator, which compete in a zero-sum game.

- **Generator**: Learns to produce data that mimics the real data distribution.
- **Discriminator**: Learns to distinguish between real data and data produced by the generator.

## How GANs Work

1. The generator creates fake data samples.
2. The discriminator evaluates both real and fake samples.
3. The generator tries to fool the discriminator, while the discriminator tries to correctly classify samples.
4. Both networks improve through training, resulting in increasingly realistic generated data.

## Mathematical Formulation

The GAN framework is defined by a minimax game between the generator $G$ and discriminator $D$:

$$
\min_G \max_D V(D, G) = 
\mathbb{E}_{x \sim p_{\text{data}}(x)} \big[\log D(x)\big] + 
\mathbb{E}_{z \sim p_z(z)} \big[\log (1 - D(G(z)))\big]
$$

Where:
- $p_{\text{data}}(x)$ is the distribution of real data.
- $p_z(z)$ is the prior distribution for the generator input noise.
- $G(z)$ is the generated sample.
- $D(x)$ is the probability that $x$ is real.

### Generator Objective

The generator aims to minimize:
$$
L_G = -\mathbb{E}_{z \sim p_z(z)} [\log D(G(z))]
$$

### Discriminator Objective

The discriminator aims to maximize:
$$
L_D = \mathbb{E}_{x \sim p_{\text{data}}(x)} [\log D(x)] + \mathbb{E}_{z \sim p_z(z)} [\log(1 - D(G(z)))]
$$

### Nash Equilibrium

At optimality, the generator produces samples indistinguishable from real data:
$$
p_g(x) = p_{\text{data}}(x)
$$

### Jensen-Shannon Divergence

GANs implicitly minimize the Jensen-Shannon divergence between $p_{\text{data}}$ and $p_g$:
$$
JS(p_{\text{data}} \|\| p_g)
$$

## Applications of GANs

- Image synthesis (e.g., generating realistic photos)
- Data augmentation
- Super-resolution
- Style transfer
- Text-to-image generation

## Example Table: GANs vs. Other Models

| Feature         | GANs                | Autoencoders      | VAEs               |
|----------------|---------------------|-------------------|--------------------|
| Adversarial?   | Yes                 | No                | No                 |
| Latent Space?  | Yes                 | Yes               | Yes                |
| Output Quality | High (if trained)   | Moderate          | Moderate           |
| Training Type  | Unsupervised        | Unsupervised      | Unsupervised       |

## References

- Goodfellow, I., et al. "Generative Adversarial Nets." NeurIPS 2014.
- https://en.wikipedia.org/wiki/Generative_adversarial_network
