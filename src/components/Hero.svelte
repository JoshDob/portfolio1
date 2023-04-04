<svg viewBox="0 0 500 500" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="gradient1" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#FFB900" />
      <stop offset="100%" stop-color="#FF4500" />
    </linearGradient>
    <linearGradient id="gradient2" x1="0%" y1="0%" x2="0%" y2="100%">
      <stop offset="0%" stop-color="#8B008B" />
      <stop offset="100%" stop-color="#00FFFF" />
    </linearGradient>
    <mask id="mask1">
      <rect x="0" y="0" width="500" height="500" fill="#fff" />
      <circle cx="250" cy="250" r="100" fill="#000" />
    </mask>
    <mask id="mask2">
      <rect x="0" y="0" width="500" height="500" fill="#fff" />
      <path d="M 0 250 Q 125 375 250 250 T 500 250 V 500 H 0 Z" fill="#000" />
    </mask>
    <mask id="mask3">
      <rect x="0" y="0" width="500" height="500" fill="#fff" />
      <circle cx="250" cy="250" r="150" fill="#000" />
    </mask>
    <mask id="mask4">
      <rect x="0" y="0" width="500" height="500" fill="#fff" />
      <path d="M 250 0 Q 375 125 250 250 T 250 500 H 0 V 0 Z" fill="#000" />
    </mask>
  </defs>

  <rect x="0" y="0" width="500" height="500" fill="url(#gradient1)" />

  <g mask="url(#mask1)">
    <rect x="0" y="0" width="500" height="500" fill="url(#gradient2)">
      <animate
        attributeName="x"
        from="-500"
        to="500"
        dur="30s"
        repeatCount="indefinite"
      />
      <animate
        attributeName="y"
        from="-500"
        to="500"
        dur="40s"
        repeatCount="indefinite"
      />
    </rect>
  </g>

  <g mask="url(#mask2)">
    <rect x="0" y="0" width="500" height="500" fill="url(#gradient1)">
      <animate
        attributeName="x"
        from="500"
        to="-500"
        dur="20s"
        repeatCount="indefinite"
      />
      <animate
        attributeName="y"
        from="500"
        to="-500"
        dur="25s"
        repeatCount="indefinite"
      />
    </rect>
  </g>

  <g mask="url(#mask3)">
    <rect x="0" y="0" width="500" height="500" fill="url(#gradient2)">
      <animate
        attributeName="x"
        from="500"
        to="-500"
        dur="35s"
        repeatCount="indefinite"
      />
      <animate
        attributeName="y"
        from="-500"
        to="500"
        dur="45s"
        repeatCount="indefinite"
      />
    </rect>
  </g>
</svg>
