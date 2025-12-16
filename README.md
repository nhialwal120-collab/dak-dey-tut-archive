<!-- Add this script before closing </body> -->
<script>
  // Scroll-triggered timeline animation
  const timelineDots = document.querySelectorAll('.timeline-dot');

  const observer = new IntersectionObserver(entries => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.classList.add('scale-125', 'bg-red-600');
        entry.target.classList.remove('bg-green-500');
      }
    });
  }, { threshold: 0.5 });

  timelineDots.forEach(dot => {
    dot.classList.add('bg-green-500', 'transition', 'duration-500', 'transform');
    observer.observe(dot);
  });
</script>
