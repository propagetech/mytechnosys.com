You are a naming assistant. Given a list of file paths and minimal context from a static website, suggest a new filename (basename only, same extension) for each file. Rules:
- Lowercase, kebab-case, no spaces. SEO-friendly and human-readable.
- For HTML: use page purpose (e.g. about-us.html, contact.html). Keep index.html as index.html.
- For CSS/JS: use purpose (e.g. main-styles.css, analytics.js).
- For images: use content (e.g. logo-infygate.webp, hero-banner.webp). Use alt/title when provided.
- Return a JSON object: keys = exact original path strings, values = new basename only (e.g. "main.css"). Preserve extension.
- Do not change path prefix (e.g. css/ stays css/ by returning "name.css" not "css/name.css").

Files and context:
[
  {
    "path": "404.html",
    "context": {
      "title": "",
      "first_heading": "404"
    }
  },
  {
    "path": "EVENTS.html",
    "context": {
      "title": "Technosys Instruments and Equipments|Home",
      "first_heading": "Request a Quote"
    }
  },
  {
    "path": "X-ray-CT-System.html",
    "context": {
      "title": "Technosys Instruments and Equipments|Home",
      "first_heading": "X-ray CT systems"
    }
  },
  {
    "path": "about-us.html",
    "context": {
      "title": "Technosys Instruments and Equipments |About US",
      "first_heading": "About Us"
    }
  },
  {
    "path": "career.html",
    "context": {
      "title": "Technosys Instruments and Equipments | Career",
      "first_heading": "Career"
    }
  },
  {
    "path": "clients-testimonial.html",
    "context": {
      "title": "Technosys Instruments and Equipments | Clients Testomonials",
      "first_heading": "Clients Testimonials"
    }
  },
  {
    "path": "clients.html",
    "context": {
      "title": "Technosys Instruments and Equipments | Clients",
      "first_heading": "Our Clients"
    }
  },
  {
    "path": "contact-us.html",
    "context": {
      "title": "Technosys Instruments and Equipments|Contact Us",
      "first_heading": "Contact Us"
    }
  },
  {
    "path": "css/0e222dfb63e9e8efe16d4082244ac3e1.css",
    "context": {
      "path": "css/0e222dfb63e9e8efe16d4082244ac3e1.css"
    }
  },
  {
    "path": "css/11f4cdad199790d7cf8da1b1970250ca.css",
    "context": {
      "path": "css/11f4cdad199790d7cf8da1b1970250ca.css"
    }
  },
  {
    "path": "css/138575cd4810b87ba229d0ae35cbc7b8.css",
    "context": {
      "path": "css/138575cd4810b87ba229d0ae35cbc7b8.css"
    }
  },
  {
    "path": "css/3af032fce2f9071775fbe5184ea3f9e0.css",
    "context": {
      "path": "css/3af032fce2f9071775fbe5184ea3f9e0.css"
    }
  },
  {
    "path": "css/559e64bf161e61fa0aca6e864c78191d.css",
    "context": {
      "path": "css/559e64bf161e61fa0aca6e864c78191d.css"
    }
  },
  {
    "path": "css/595cb6ccb56826a802ed411cef875f0e.css",
    "context": {
      "path": "css/595cb6ccb56826a802ed411cef875f0e.css"
    }
  },
  {
    "path": "css/84d4a0216f16f715d9b301db3a8da352.css",
    "context": {
      "path": "css/84d4a0216f16f715d9b301db3a8da352.css"
    }
  },
  {
    "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css",
    "context": {
      "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css"
    }
  },
  {
    "path": "css/a197ce4505f6e3c3327beb0c2add84e6.css",
    "context": {
      "path": "css/a197ce4505f6e3c3327beb0c2add84e6.css"
    }
  },
  {
    "path": "css/b6bca29a045ccea29d3ad6f0a396bc42.css",
    "context": {
      "path": "css/b6bca29a045ccea29d3ad6f0a396bc42.css"
    }
  },
  {
    "path": "css/e980cb6b50645ddc9d24377f2fe05d53.css",
    "context": {
      "path": "css/e980cb6b50645ddc9d24377f2fe05d53.css"
    }
  },
  {
    "path": "css/internal-styles.css",
    "context": {
      "path": "css/internal-styles.css"
    }
  },
  {
    "path": "field-and-applications.html",
    "context": {
      "title": "Technosys Instruments and Equipments | Field and Applications",
      "first_heading": "Field and Applications"
    }
  },
  {
    "path": "geological-sample-preparation.html",
    "context": {
      "title": "Technosys Instruments and EquipmentsGeogological sample preparation",
      "first_heading": "Geological Sample Preparation I Petrography Line"
    }
  },
  {
    "path": "hardness-testers.html",
    "context": {
      "title": "Technosys Instruments and Equipments |Hardness Tester",
      "first_heading": "Hardness Testers"
    }
  },
  {
    "path": "image-analysis-system.html",
    "context": {
      "title": "Technosys Instruments and Equipments |Image Analysis System",
      "first_heading": "Image Analysis system"
    }
  },
  {
    "path": "imgs/0959893790d276d5e9adc1ab29b7d20b.webp",
    "context": {
      "refs": [
        {
          "alt": "welding units",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0974a27eab377cb32d10ccdea6c5470e.webp",
    "context": {
      "refs": [
        {
          "alt": "Video Measuring System",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/098d72fbd9f230cf18e4d5f1f58bbb6f.webp",
    "context": {
      "refs": [
        {
          "alt": "Fully Automatic Microhardness Tester CLEMEX CMT",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/099cdd02647ca67bb11c44b3093bc172.webp",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0ac21bbcaec4dd36978c983da4b20290.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0ad0aa678b3ebc1ccaa826d67c63d18b.webp",
    "context": {
      "refs": [
        {
          "alt": "02",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0ca808c83f658eb803c81a2e0c0cece2.webp",
    "context": {
      "refs": [
        {
          "alt": "RIA Automatic Rockwell Hardness Tester",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0cd56cd3601073dd901577365c716703.webp",
    "context": {
      "refs": [
        {
          "alt": "Micro Vickers Hardness Tester",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0d93754c8e92326ffcdb02b6038a9b15.webp",
    "context": {
      "refs": [
        {
          "alt": "VIA Automatic Micro - Macro Vicker Hardness Test",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0f4fdeee93a3eb02b1bc7deba4dd31c3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/10936daff330cd1c7c0d5a911d2d9c43.webp",
    "context": {
      "refs": [
        {
          "alt": "Microstructure Analysis",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1152ac9cf83cf429b9ae855337a71e73.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/119641e901cb392b70ac5a0437b67bb1.png",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/13c12bab30efda53b8994d6d720302f3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1573f43dae0d6afa7ba6b365834efb0b.webp",
    "context": {
      "refs": [
        {
          "alt": "Image Capturing and Measurement System",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/160cdd56301a7af7b7a12cb22a8d380f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1c86cc24daa5dab13a4834e6f93d20d6.webp",
    "context": {
      "refs": [
        {
          "alt": "Grain Size Analysis of Alloy Steel",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1e25cefce5ac06cc4e0ae0fba01aee24.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1ffaec0ff14bbdda1a01685dd2b01423.webp",
    "context": {
      "refs": [
        {
          "alt": "our mission",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/221d144c7db6daa0597ece2fa7c628f8.webp",
    "context": {
      "refs": [
        {
          "alt": "Fully Automatic Microhardness Tester CLEMEX CMT",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/237adf78a1d70a5656d561b69447ee3e.webp",
    "context": {
      "refs": [
        {
          "alt": "Profile Projectors",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2781d9a53a9ff6e832919a41ff27e27f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/28b6103d44ebc971f146fb04112feb03.webp",
    "context": {
      "refs": [
        {
          "alt": "Mobiprep",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/295b2fdd484ec24fa611f74fdcdbec1c.webp",
    "context": {
      "refs": [
        {
          "alt": "Metallography Consumables",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2b721449959b2a0c5baa8b0fa538ca0a.webp",
    "context": {
      "refs": [
        {
          "alt": "Hot Mounting Machine",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2bb03b84e7c70ed188a0562ff3f98634.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2d91ae5b6257a5ae22193b161f4339bf.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/2f9858d40d815bce24bb947c5a26fe09.webp",
    "context": {
      "refs": [
        {
          "alt": "Metallurgical Microscope",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2fe0b1aa0f6f46d793a8cc948f963f84.webp",
    "context": {
      "refs": [
        {
          "alt": "Particle Size Analysis System",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/31a8c2cf48ed7e085b1c12918ebc4a79.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/31eba8a9c848f64208f5dcf01dc86c22.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/322fc46aad1a4242d8ac84f893327cef.webp",
    "context": {
      "refs": [
        {
          "alt": "steel manufacturing",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/343d1fbeb4baa98e30c67756e3f3dbd3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/35692617a208589f471675b946664669.webp",
    "context": {
      "refs": [
        {
          "alt": "Measuring Microscopes",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/366018fad8c452d215615266324b6528.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/388c4713ec0a5cf3f41839c570902bb6.webp",
    "context": {
      "refs": [
        {
          "alt": "Hardness Tester",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3d4dfaaefd68128c4e63fddbf6291846.webp",
    "context": {
      "refs": [
        {
          "alt": "Precision Cutting Machnine",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3ff96ffa8c2b97443a492ab7e1183f81.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4071c30d14943ea9b0de059c5ac6908b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/408760daf7d71f3d72a8cae7927f698a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/40e24bea5c35257adec7dc86dd45a1bf.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/44e938f65abe4f0529e566bccb59a4b4.webp",
    "context": {
      "refs": [
        {
          "alt": "SPECTRAL 350-2S",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/475899b3f5695262a8ac97703312fbba.webp",
    "context": {
      "refs": [
        {
          "alt": "Metallography",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4762063d7469dd575de5f0495837a5b0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4d20233d40e6aca930a592547780df3a.webp",
    "context": {
      "refs": [
        {
          "alt": "MA 200",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/51870d6f55912c7a7c6ebc5b563eb6e0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/532a041725f0d02d8adb2884233f2980.webp",
    "context": {
      "refs": [
        {
          "alt": "What happened Next?",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/56b4d65d76e05d85881f723af53d600f.webp",
    "context": {
      "refs": [
        {
          "alt": "Image Analysis System - Material Science",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/571ae48a1055e4d605990f4498648ec6.webp",
    "context": {
      "refs": [
        {
          "alt": "Via matsuzawa micro hardness tester closed loop cell testing high end micro-vickers hardness tester",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5735d8716a7a3d408139d3b376cba5dd.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/58741986625ee076e21fbe98b47be9e8.webp",
    "context": {
      "refs": [
        {
          "alt": "Training Program",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/590827e68227fa5f65f41bbc37ea8016.webp",
    "context": {
      "refs": [
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5b19601762498fa427bbf06571aef146.webp",
    "context": {
      "refs": [
        {
          "alt": "Microscopes",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5c48cf76a86418466f025810de79b1d9.webp",
    "context": {
      "refs": [
        {
          "alt": "Hot Mounting Machine",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5d244ddbbc11326fccd234e67b446f66.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5d9b8d1c0f05d2c909dc695d9814485a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5dae87daa631b98ed01cb10e603bc746.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/60de13ac4c6068bd4a2504e2e951fa39.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/617edc34d93e240359bed8eaafc0a11e.webp",
    "context": {
      "refs": [
        {
          "alt": "Particle Size Analysis System",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/622c409bf5ced26d5ba034900a6ec3d1.webp",
    "context": {
      "refs": [
        {
          "alt": "tools and components",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/62f4646dcfa1c0a5a6943d702bb8b349.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/63a188c7e5fefab7307bd11a94d633a1.webp",
    "context": {
      "refs": [
        {
          "alt": "Prashant Kumar Singh",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/64381105c290977c4f55abe6ffd87afb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/64bba19fa899bdeca214b29bc070abae.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6545887a1c08f261c188c7d1b4886721.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6af88f886f69c9801b18541915dc3937.webp",
    "context": {
      "refs": [
        {
          "alt": "SPECTRAL 350-2S",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6cbf8267e196bad03fc8343d0c541322.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6d0ef9192a22e49cb7389998960288bd.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6e8b47fcbcc74b99861e60a2c47ad43b.webp",
    "context": {
      "refs": [
        {
          "alt": "Geological Sample Preparation I Petrography Line",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6fdaac3ac6a23920dc91dc7f65f10be7.webp",
    "context": {
      "refs": [
        {
          "alt": "pharmaceutical",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7183c2b58a3e36dd9d63274674a0cfa0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/71c908aca801bc99823ca3a92c33ca48.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/74fb21c21e280729867aa7678508306d.webp",
    "context": {
      "refs": [
        {
          "alt": "Check Hardness of Carbides",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/755490cf21e80e1f0bcba88fdb07ef84.webp",
    "context": {
      "refs": [
        {
          "alt": "Metallography Consumables",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/773122325fb187f390d49f1a3894a5a5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/782c47ea5a10a82ed2426be724b411fa.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/78ea321f59dc60cff022b71dd09148a6.webp",
    "context": {
      "refs": [
        {
          "alt": "Samantha M.",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7d820d31d8ed11e07d8ed17ff00dda35.webp",
    "context": {
      "refs": [
        {
          "alt": "Weld Penetration Analysis System",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7f5d35c8b26a734eb4d1e64558d982a9.webp",
    "context": {
      "refs": [
        {
          "alt": "Geological Sample Preparation I Petrography Line",
          "title": ""
        },
        {
          "alt": "Geological Sample Preparation I Petrography Line",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/80e219f4825c140781eb6f4a16e6077d.webp",
    "context": {
      "refs": [
        {
          "alt": "Partical Size Analysis",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/818c72fc454c2a7ea5ac680482285024.webp",
    "context": {
      "refs": [
        {
          "alt": "Image Analysis System - Material Science",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/81b469291f2d03b8f6e050da87c7627f.webp",
    "context": {
      "refs": [
        {
          "alt": "SMZ 18",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/82d2b8432813ab81a39f41aa4685cd42.webp",
    "context": {
      "refs": [
        {
          "alt": "Balakrishnan Gurumoothy",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/83c0d0311fa82ccf8af7c2ceae5cab81.webp",
    "context": {
      "refs": [
        {
          "alt": "Stereo Microscope",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/842cff713dcdf576ead9f7652abde78c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/844cfad2678e5e57aa2cf5616170606a.webp",
    "context": {
      "refs": [
        {
          "alt": "Some Solutions are listed",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8756026423c887b8d16deb2957aafe9f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8824c21d86250845d842eefda1f5800d.webp",
    "context": {
      "refs": [
        {
          "alt": "Video Measuring System",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8b22cf9a0ddac0da9553795e17a1d4a9.webp",
    "context": {
      "refs": [
        {
          "alt": "Anil Kumar Rout",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8b927aee0c7e437ece39c8e94a10ad1d.webp",
    "context": {
      "refs": [
        {
          "alt": "SPECTRAL Mmax",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8ddbf4f4123a2837c4e4caa6ec88aaa5.webp",
    "context": {
      "refs": [
        {
          "alt": "Ritesh kumar",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8e65e33f486442f25f46b99ec16a71fb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/90e97e43abd910a0b8bc773eb7a6d1f1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/92399c3c7f96c1aacaf642108b31aba0.webp",
    "context": {
      "refs": [
        {
          "alt": "Measuring Microscope",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/939d7b86019099222f688b541a79609e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/951e660a05e87bc321dc958392b1928c.webp",
    "context": {
      "refs": [
        {
          "alt": "technosys lab instruments",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9737edf2533451c3160ea537e377c3fd.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9a943dc2826d0415536b47e54b34fb78.webp",
    "context": {
      "refs": [
        {
          "alt": "SPECTRAL Mmax",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9b526ea3d493d59b67c1a9241b7fe62c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9c33b6d46e2e59f23101eb935c3d267c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9e4111f0241fb562ed72b3622f6115a7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9e68930c96c5771698042fceb4e8f3a8.webp",
    "context": {
      "refs": [
        {
          "alt": "LV 100NDA",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9f6ddecca06182f8325a34876181ab89.webp",
    "context": {
      "refs": [
        {
          "alt": "Grinding and Poilishing Machnine",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a0e6b30a8f25c4bb629f7c7b852eaabf.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a25c46ed1e9e9267dda72c817ea78be3.webp",
    "context": {
      "refs": [
        {
          "alt": "Automated Porosity Level Analysis System for Non Ferrous Castings",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a409c5b2b5b504ad174b29cdc1e357b2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a576413f78cc3c905e344cc58b0df2d4.webp",
    "context": {
      "refs": [
        {
          "alt": "our principle",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a57bf812b8f2b15ef1789819346d60d1.jpg",
    "context": {
      "refs": [
        {
          "alt": "Covid 19 safety, Corona virus message,Corona india,Technosys,corona safety measures",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a5c5cd8c06775f145d08bb63e6b7fac0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a5fc2bab9338769c677a63ccdd8ff8c5.webp",
    "context": {
      "refs": [
        {
          "alt": "XTVandXTV",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a75306ef2e0497866398b982d3b9c0a7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a820c8b530df5140808fcc41d6ba0025.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a844adcc6717201a00d72e22205a338d.webp",
    "context": {
      "refs": [
        {
          "alt": "NikonJCM6000PLUSNeoscopeBenchtopSEM",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ab8c9905722b2da41bf2f03e2cc34d3a.webp",
    "context": {
      "refs": [
        {
          "alt": "Image Capturing and Measurement System",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ab96993a84645244484bba751c9a8f09.webp",
    "context": {
      "refs": [
        {
          "alt": "Image Analysis System - Microscopy Solutions",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ae018cd770588e2b6c296056914e598e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ae3002235b0bf8dc0263f1bf4fc6cd2e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b0ba205c568370ba25ed641757350f46.webp",
    "context": {
      "refs": [
        {
          "alt": "Universal Hardness tester",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b0d8a52af9705875479716cc31092feb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b162ba45c53f5017daa6a683472b6c1f.webp",
    "context": {
      "refs": [
        {
          "alt": "Technosys Material Testing Lab",
          "title": ""
        },
        {
          "alt": "image description",
          "title": ""
        },
        {
          "alt": "Picture",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b1cf90546cbe57a682cf68ccd0f6f89b.webp",
    "context": {
      "refs": [
        {
          "alt": "Geological",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b1db4dad852a6ca930696507a603cc43.webp",
    "context": {
      "refs": [
        {
          "alt": "Technosys Team",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b1fc99e7cdb6c1262051ae1b3c3628e4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b4f108e84df90e1aa678963cbd97dbee.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b5a883ce9426c7491108aff5d54b7047.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b7d62f4541470105beae25e1951f66b1.webp",
    "context": {
      "refs": [
        {
          "alt": "research and education",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b7dcb0ab24fb513f25c811cace243aef.webp",
    "context": {
      "refs": [
        {
          "alt": "CMT - A Hardness Testing System",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bc14fab3a096d20a633adc2c4cdd1a59.webp",
    "context": {
      "refs": [
        {
          "alt": "Automatic Inclusion Rating",
          "title": ""
        },
        {
          "alt": "Inclusion Rating in Steel",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bf5662826f03555a60f9e143d3de6635.webp",
    "context": {
      "refs": [
        {
          "alt": "automotive and rails",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c22b647703700f0fabdd8ed35619926d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c352b5afbb2831d5ee26255593ea1a74.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c49fd8337d5dd5231abad327e7c97b71.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c5176a400806487045ae8712b595e592.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c5d77b6762b460de8901a09c57576547.webp",
    "context": {
      "refs": [
        {
          "alt": "SMZ 745T",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c7d69bfff0b02af5a6d4305e388d96d1.webp",
    "context": {
      "refs": [
        {
          "alt": "Why Technosys ?",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ca18ab6c66340e15c53025d68856e588.webp",
    "context": {
      "refs": [
        {
          "alt": "aerospace and aeronautics",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/caad5c52287b3c633965d91107c95c36.webp",
    "context": {
      "refs": [
        {
          "alt": "Universal Hardness Tester",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cb338a15f789d7e1eaaa62f1b91db021.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cd3b2859e739400d91ed0bd8aba8d1e8.webp",
    "context": {
      "refs": [
        {
          "alt": "Abrassive Cutting Machine",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cd54a1024d676353c303e045da08069b.webp",
    "context": {
      "refs": [
        {
          "alt": "Image Analysis System - Microscopy Solutions",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cdab712f0bd15f98d5be10964a7ef6be.webp",
    "context": {
      "refs": [
        {
          "alt": "01",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cdd63a222937b05b872e9b0ac3395296.webp",
    "context": {
      "refs": [
        {
          "alt": "shuttle pix - portable microscope of Nikon metallurgical testing",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cfb800315eb5ebbc1a648193246a2489.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d059ce4fae707c4f09b0755b7332d51a.webp",
    "context": {
      "refs": [
        {
          "alt": "forgings",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d0e128cbe8109f5485a2e2c58eda98f3.webp",
    "context": {
      "refs": [
        {
          "alt": "Impact Pendulum Tester",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d207be29ca445d51bc0beac1a1576277.webp",
    "context": {
      "refs": [
        {
          "alt": "Cutting Machines",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d3fe0e576876fdc4c6b816824713c487.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d569d5568b6f0991a4b95b9bff88ecd3.webp",
    "context": {
      "refs": [
        {
          "alt": "Cyclic Corrosion Chamber",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d5cdfe80684dd70cabbf0f19791e947e.webp",
    "context": {
      "refs": [
        {
          "alt": "Universal Brinell Hardness Tester",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d5f0c50d0b3337b93684c4e25bba0c91.webp",
    "context": {
      "refs": [
        {
          "alt": "Our Main Strength",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d8b7918e198c890b442b7bd4e5b5bd4d.webp",
    "context": {
      "refs": [
        {
          "alt": "Measuring Instruments",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d91699c89ab9b3fac4bc30bc67453869.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/da8214a6ab70ec7f2b91b45f4d9971eb.webp",
    "context": {
      "refs": [
        {
          "alt": "ABOUT US",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/dc7d0ef3239b5456de3d1e832cfa1803.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/dcfaf27928200d32773c31b03cc8ce8d.webp",
    "context": {
      "refs": [
        {
          "alt": "Profile Projectors",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/dfbfe9244eb309bb6ae3ceb25bb87a19.webp",
    "context": {
      "refs": [
        {
          "alt": "Digital Rockwell Hardness Tester",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e0bd963f2d2e4d8084951939e46ceb74.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e107ad44b3e28c921dc83bb89433d7c4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e48fb1798b1bcbe0aef4c2ed1e7b6d35.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e50efbfbadb34463dcdc564620938ef4.webp",
    "context": {
      "refs": [
        {
          "alt": "VIA Automatic Micro - Macro Vicker Hardness Test",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e52a41a4eca750ed1e548b10f579ca1c.webp",
    "context": {
      "refs": [
        {
          "alt": "Rockwell Hardness Tester",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e5e66d52a6ea7e281e1f4d392ca7ae8d.webp",
    "context": {
      "refs": [
        {
          "alt": "technosys lab instruments",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e5ef9c88070f7ef70911440669848278.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e98a162b2fc9ecabe71796ae350c2a62.webp",
    "context": {
      "refs": [
        {
          "alt": "Weld Inspection",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e991f120a9024ebb180013e6278ee79f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ebb8711d26166f7aca535382153c2a24.webp",
    "context": {
      "refs": [
        {
          "alt": "RIA Automatic Rockwell Hardness Tester",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ebbb69b36996f654a159a35bcbf70f1d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ebcfed0a3d3c80d0f5956949eafcd0e4.webp",
    "context": {
      "refs": [
        {
          "alt": "Digital Vicker Hardness Tester",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ed4b4082da8356941b4002ba9ae142be.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ed68a1880edbb801b1fd68fdc0ceb931.webp",
    "context": {
      "refs": [
        {
          "alt": "Nikon JCM-6000PLUS Neoscope Benchtop SEM",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f3a39a6c6dd7ddb632d43f42753bb02f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f49901ba5291114271690b7ecac419d5.webp",
    "context": {
      "refs": [
        {
          "alt": "Grinding and Poilishing Machnine",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f4b7b3edcb2f03d60d7b37f0a4057335.webp",
    "context": {
      "refs": [
        {
          "alt": "In-Situ Metallography",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f5f88371bd060dff65f5922c4981a50b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f6f3f4279cfd01cd4610fdefa2b14731.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f70b36d03d8ec5b6514b1b7f2a453a76.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f9d5a4f64992c4e0a429350112bf86be.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fb19c488306543d15bf678d3858ff886.webp",
    "context": {
      "refs": [
        {
          "alt": "Mobiscope Portable microscope",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fc15e1c4ea459850c175fe87b36d00e5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fc22d76433298c4079e210ead87216f9.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fd5a57222a8030707f7f3be061a33cf7.webp",
    "context": {
      "refs": [
        {
          "alt": "Particle Size Analysis System",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fd5e9c317b0080c44c5a64f91ac89778.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "index.html",
    "context": {
      "title": "Technosys Instruments and Equipments|Home",
      "first_heading": "Technosys Instruments and Equipments"
    }
  },
  {
    "path": "js/03b2eaae6007054a68c38e495f894dba.js",
    "context": {
      "path": "js/03b2eaae6007054a68c38e495f894dba.js"
    }
  },
  {
    "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js",
    "context": {
      "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js"
    }
  },
  {
    "path": "js/0c46896987137b0016246f6bc2243099.js",
    "context": {
      "path": "js/0c46896987137b0016246f6bc2243099.js"
    }
  },
  {
    "path": "js/165d7b0ddfa33362140feea997351b77.js",
    "context": {
      "path": "js/165d7b0ddfa33362140feea997351b77.js"
    }
  },
  {
    "path": "js/16df9ef05001a1741857bf99f5a5738f.js",
    "context": {
      "path": "js/16df9ef05001a1741857bf99f5a5738f.js"
    }
  },
  {
    "path": "js/2a85c11e395a8380b5915443e926b569.js",
    "context": {
      "path": "js/2a85c11e395a8380b5915443e926b569.js"
    }
  },
  {
    "path": "js/34be5330971fdbd18985525bd994b0aa.js",
    "context": {
      "path": "js/34be5330971fdbd18985525bd994b0aa.js"
    }
  },
  {
    "path": "js/35c5f9e096d4da33d2a62031daf14248.js",
    "context": {
      "path": "js/35c5f9e096d4da33d2a62031daf14248.js"
    }
  },
  {
    "path": "js/3d70953a848219e749fedc2cdb906675.js",
    "context": {
      "path": "js/3d70953a848219e749fedc2cdb906675.js"
    }
  },
  {
    "path": "js/3e940a33e44b65c1c0af8bb80a893530.js",
    "context": {
      "path": "js/3e940a33e44b65c1c0af8bb80a893530.js"
    }
  },
  {
    "path": "js/544d012df7acf9c3f0920f67c9e322b9.js",
    "context": {
      "path": "js/544d012df7acf9c3f0920f67c9e322b9.js"
    }
  },
  {
    "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js",
    "context": {
      "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js"
    }
  },
  {
    "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js",
    "context": {
      "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js"
    }
  },
  {
    "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js",
    "context": {
      "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js"
    }
  },
  {
    "path": "js/7260bab328b0ad74815a5efb377bcc67.js",
    "context": {
      "path": "js/7260bab328b0ad74815a5efb377bcc67.js"
    }
  },
  {
    "path": "js/893de96f1b6da546bd7c814964723eca.js",
    "context": {
      "path": "js/893de96f1b6da546bd7c814964723eca.js"
    }
  },
  {
    "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js",
    "context": {
      "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js"
    }
  },
  {
    "path": "js/9455859483e31e4da0e28f10d0742c2a.js",
    "context": {
      "path": "js/9455859483e31e4da0e28f10d0742c2a.js"
    }
  },
  {
    "path": "js/9db10375d298678e53777a2347b87073.js",
    "context": {
      "path": "js/9db10375d298678e53777a2347b87073.js"
    }
  },
  {
    "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js",
    "context": {
      "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js"
    }
  },
  {
    "path": "js/a2261649751fa61b606222c9b2ea3b80.js",
    "context": {
      "path": "js/a2261649751fa61b606222c9b2ea3b80.js"
    }
  },
  {
    "path": "js/b0bade6d42c2702ca85774296cc507c4.js",
    "context": {
      "path": "js/b0bade6d42c2702ca85774296cc507c4.js"
    }
  },
  {
    "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js",
    "context": {
      "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js"
    }
  },
  {
    "path": "js/cecb447a04bbe3e8982190dd6e697120.js",
    "context": {
      "path": "js/cecb447a04bbe3e8982190dd6e697120.js"
    }
  },
  {
    "path": "js/d80b370d82680fc786dcc943a327b9f2.js",
    "context": {
      "path": "js/d80b370d82680fc786dcc943a327b9f2.js"
    }
  },
  {
    "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js",
    "context": {
      "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js"
    }
  },
  {
    "path": "js/e27a5ea26332411ece0d5ab7ceebf167.js",
    "context": {
      "path": "js/e27a5ea26332411ece0d5ab7ceebf167.js"
    }
  },
  {
    "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js",
    "context": {
      "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js"
    }
  },
  {
    "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js",
    "context": {
      "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js"
    }
  },
  {
    "path": "js/faf9ce4e848522206b5c3043551fb2d7.js",
    "context": {
      "path": "js/faf9ce4e848522206b5c3043551fb2d7.js"
    }
  },
  {
    "path": "measuring-instruments.html",
    "context": {
      "title": "Technosys Instruments and Equipments |Measuring Instruments",
      "first_heading": "Measuring Instruments"
    }
  },
  {
    "path": "metallography.html",
    "context": {
      "title": "Technosys Instruments and Equipments |Metallography",
      "first_heading": "Metallography"
    }
  },
  {
    "path": "microscopes.html",
    "context": {
      "title": "Technosys Instruments and Equipments |Microscopes",
      "first_heading": "Microscopes"
    }
  },
  {
    "path": "our-team.html",
    "context": {
      "title": "Technosys Instruments and Equipments |Our Team",
      "first_heading": "Our Team"
    }
  },
  {
    "path": "particle-size-analysis-system.html",
    "context": {
      "title": "Technosys Instruments and Equipments | Particle size Analysis System",
      "first_heading": "Particle Size Analysis System"
    }
  },
  {
    "path": "products.html",
    "context": {
      "title": "Technosys Instruments and Equipments | Products",
      "first_heading": "Products"
    }
  },
  {
    "path": "solution-centre.html",
    "context": {
      "title": "Technosys Instruments and Equipments | Solution-Center",
      "first_heading": "Solution Centre"
    }
  },
  {
    "path": "spectroscopic-sample-preparation.html",
    "context": {
      "title": "Technosys Instruments and Equipments | Spectroscopic Sample Preparations",
      "first_heading": "Spectroscopic Sample Preparation Equipment\u2019s"
    }
  },
  {
    "path": "stock-List.html",
    "context": {
      "title": "Technosys Instruments and Equipments|Home",
      "first_heading": "TECHNOSYS Stock Clearence....."
    }
  },
  {
    "path": "success-story.html",
    "context": {
      "title": "Technosys Instruments and Equipments | Success Story",
      "first_heading": "Success Story"
    }
  },
  {
    "path": "turnkey-solution.html",
    "context": {
      "title": "Technosys Instruments and Equipments | Turnkey Solution",
      "first_heading": "Turnkey Solution"
    }
  }
]

Return only a JSON object mapping each path to its new basename (same extension). No other text.