.container {
  display: grid;

  /* Define grid rows */
  grid-template-rows: 
    80vh               /* First row: 80% of the viewport height */
    min-content        /* Second row: height based on the content */
    40vw               /* Third row: 40% of the viewport width (likely a typo) */
    repeat(3, min-content);  /* Fourth to sixth rows: height based on the content */

  /* Define grid columns */
  grid-template-columns:
    [sidebar-start] 8rem  /* First column: fixed width of 8rem */
    [sidebar-end full-start] minmax(6rem, 1fr)  /* Second column: min 6rem, max 1fr */
    [center-start] repeat(8, [col-start] minmax(min-content, 14rem) [col-end])  /* Eight center columns: min content size, max 14rem */
    [center-end] minmax(6rem, 1fr)  /* Column after center: min 6rem, max 1fr */
    [full-end];  /* End of the columns */
}