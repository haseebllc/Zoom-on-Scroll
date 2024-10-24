```hash
const image = document.querySelector(".zoom-image");

window.addEventListener("scroll", () => {
    const section2 = document.querySelector(".section2");
    const section2Rect = section2.getBoundingClientRect();

    const scrollPercentage =
        (window.scrollY + window.innerHeight - section2Rect.top) /
        section2Rect.height;
    const scale = 1 + scrollPercentage * 0.2; // Adjust zoom amount here
    image.style.transform = `scale(${scale})`;
});
```
