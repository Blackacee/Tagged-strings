# Tagged-strings

function settings(strings, ...substitutions) {
 const result = new Map();
 for (let i = 0; i < substitutions.length; i++) {
 result.set(strings[i].trim(), substitutions[i]);
 }
 return result;
}
const remoteConfiguration = settings`
 label ${'Content'}
 servers ${2 * 8 + 1}
 hostname ${location.hostname}
`;
Map {"label" => "Content", "servers" => 17, "hostname" => "stackoverflow.com"}
