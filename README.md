# Rotate-CIImage

func rotate(_ angle: CGFloat) -> CIImage {
        let transform = CGAffineTransform(translationX: extent.midX, y: extent.midY)
            .rotated(by: angle)
            .translatedBy(x: -extent.midX, y: -extent.midY)
        return applyingFilter("CIAffineTransform", parameters: [kCIInputTransformKey: transform])
        }
