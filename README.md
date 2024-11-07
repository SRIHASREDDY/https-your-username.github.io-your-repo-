export default function json2html(data) {
  const headers = ["Name", "Age", "Gender"];
  let table = `<table data-user="srihasreddy9030@gmail.com"><thead><tr>`;

  headers.forEach(header => table += `<th>${header}</th>`);
  table += `</tr></thead><tbody>`;

  data.forEach(row => {
    table += `<tr><td>${row.Name}</td><td>${row.Age}</td>`;
    table += row.Gender ? `<td>${row.Gender}</td></tr>` : `</tr>`;
  });

  table += `</tbody></table>`;
  return table;
}
