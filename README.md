# On the Adversarial Robustness of Visual Transformer

Code for our paper "On the Adversarial Robustness of Visual Transformers"

Paper link: <a href="https://arxiv.org/abs/2103.15670"> https://arxiv.org/abs/2103.15670 </a>

## White-box attack test

To test adversarial robustness under white-box attack
```
python3 white_box_test.py --data_dir $DATA_DIR --mode foolbox --model vit_small_patch16_224 --pretrained
```
- The `--mode` flag decides the evaluation approach: 
    - `--mode=foolbox` applies a single attack (default: LinfPGD) for evalution.
    - `--mode=auto` applies AutoAttack for evaluation.
    - `--mode=foolbox-filter` applies the frequency-based attack for evaluation.
    - `--mode=evaluate` evaluates the clean accuracy.
    - `--mode-count` counts the number of parameters.

## Black-box attack test

To test the transferability of adversarial examples generated by different models
```
python3 black_box_test.py --data_dir $DATA_DIR
```
