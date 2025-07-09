# INSAT-CloudMotion-Forecast
Forecasting cloud motion using INSAT-3DR imagery and 3D U-Net + SE with DDIM loss .
# 🌥️ INSAT-3DR Cloud Motion Forecasting

We present a deep learning pipeline to forecast cloud motion using indigenous satellite imagery from INSAT-3DR. We leverage a 3D U-Net with SE blocks and a hybrid loss (MSE + SSIM + LPIPS) on multi-spectral channels (TIR1 + WV).

## 🚀 Key Highlights

- **Input**: 3 frames (t-60, t-30, t) from TIR1 and WV
- **Output**: Forecast of next 2 frames (t+30, t+60)
- **Backbone**: 3D U-Net with SE Blocks
- **Loss Function**: MSE + SSIM + LPIPS (per-channel, per-frame)
- **Metrics**:
  - **TIR1 Avg**: MSE=0.023, PSNR=15.39 dB, SSIM=0.6011, LPIPS=0.0913
  - **WV Avg**: MSE=0.0343, PSNR=14.67 dB, SSIM=0.5558, LPIPS=0.1266
  - **Combined Avg**: MSE=0.0318, PSNR=15.03 dB, SSIM=0.5799, LPIPS=0.1104

## 📊 Sample Output
![image](https://github.com/user-attachments/assets/61704903-11a0-4e18-9cea-045577e763ed)

