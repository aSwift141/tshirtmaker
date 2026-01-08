# T-Shirt AI Design Generator

An AI-powered web application for generating custom t-shirt designs using PiAPI's Gemini 2.5 Flash image generation.

## Features

- **JSON Style Guide**: Optional JSON input to guide the design style
- **Reference Images**: Upload reference images to inspire the AI
- **Custom Prompts**: Describe your desired t-shirt design in natural language
- **Batch Generation**: Generate multiple design variations at once
- **Design Editing**: Select any generated design and apply specific edits
- **Beautiful UI**: Clean, modern interface built with Tailwind CSS

## Getting Started

### Prerequisites

1. Get a PiAPI key from [https://piapi.ai](https://piapi.ai)
2. A modern web browser (Chrome, Firefox, Safari, Edge)

### Installation

1. Clone or download this repository
2. Open `index.html` in your web browser
3. Enter your PiAPI key in the configuration section

That's it! No build process or dependencies required.

## How to Use

### Step 1: Configure API Key
- Enter your PiAPI key in the "API Configuration" section
- The key will be saved locally in your browser for convenience

### Step 2: Input Design Parameters

#### JSON Style Guide (Optional)
Provide a JSON object to guide the design style:
```json
{
  "style": "minimalist",
  "colors": ["black", "white", "gold"],
  "theme": "geometric",
  "mood": "modern"
}
```

#### Reference Images (Optional)
- Upload one or more images to inspire the design
- Supported formats: JPG, PNG, GIF, WebP
- Images will be sent to the AI as visual references

#### Design Prompt (Required)
Describe your t-shirt design in detail:
- "A fierce dragon wrapped around a mountain with cherry blossoms"
- "Minimalist geometric lion head in black and gold"
- "Retro 80s sunset with palm trees and neon colors"

### Step 3: Set Quantity
- Choose how many design variations you want (1-10)
- Each design will be generated sequentially

### Step 4: Generate Designs
- Click "Generate Designs" and wait for the AI to create your designs
- Progress will be shown in real-time
- Generated designs will appear in a gallery

### Step 5: Edit Specific Designs (Optional)
- Click "Select for Editing" on any design
- Describe the changes you want in the edit prompt
- Click "Apply Edits" to generate an updated version
- The original design will be replaced with the edited version

## Design Guidelines

The AI is instructed to create designs with the following characteristics:
- **30-50% negative space** for a clean, professional look
- **Plain background** to focus on the design itself
- **No mockup** - just the design elements
- **T-shirt ready** - suitable for printing

## API Information

This application uses the PiAPI Gemini 2.5 Flash image generation API:
- **Endpoint**: `https://api.piapi.ai/api/v1/task`
- **Model**: `gemini-2.0-flash-exp`
- **Aspect Ratio**: 1:1 (square images)

### API Request Format

The application sends requests in the following format:
```javascript
{
  "prompt": "Your combined prompt here",
  "model": "gemini-2.0-flash-exp",
  "image_num": 1,
  "aspect_ratio": "1:1",
  "images": ["base64_image_data"] // Optional reference images
}
```

## Tips for Best Results

1. **Be Specific**: Detailed prompts generate better results
   - Bad: "cool design"
   - Good: "geometric wolf head with constellation patterns, minimal line art style"

2. **Use Style Guides**: The JSON field helps maintain consistent aesthetics
   - Define color palettes, art styles, moods, and themes

3. **Reference Images**: Upload similar designs or inspiration images
   - The AI will use these to understand your visual preferences

4. **Iterate with Edits**: Don't expect perfection on the first try
   - Generate multiple variations
   - Select the best one and refine it with specific edit instructions

5. **Consider Printing**: Remember these designs will be printed on t-shirts
   - Avoid overly complex details that won't print well
   - Keep text readable if included
   - Ensure good contrast

## Troubleshooting

### "API request failed"
- Check that your API key is correct
- Ensure you have credits remaining in your PiAPI account
- Check your internet connection

### "Timeout waiting for image generation"
- The image is taking longer than expected
- Try simplifying your prompt
- Try again with fewer reference images

### Designs not appearing
- Check the browser console (F12) for error messages
- Ensure your PiAPI key has the necessary permissions
- Try refreshing the page and generating again

### Images won't upload
- Check file size (keep under 5MB per image)
- Ensure images are in supported formats (JPG, PNG, GIF, WebP)
- Try uploading fewer images at once

## Browser Compatibility

- Chrome/Edge: Fully supported ✓
- Firefox: Fully supported ✓
- Safari: Fully supported ✓
- Internet Explorer: Not supported ✗

## Privacy & Security

- Your API key is stored locally in your browser (localStorage)
- No data is sent to any server except PiAPI
- Reference images are converted to base64 and sent directly to PiAPI
- No tracking or analytics

## License

This project is open source and available for personal and commercial use.

## Support

For issues with:
- **This application**: Open an issue on the GitHub repository
- **PiAPI service**: Contact PiAPI support at https://piapi.ai
- **API documentation**: Visit https://piapi.ai/docs/gemini-api/gemini-25-flash-image

## Credits

- Built with [Tailwind CSS](https://tailwindcss.com)
- Powered by [PiAPI](https://piapi.ai) and Google's Gemini AI
- Created for t-shirt designers and creative entrepreneurs
