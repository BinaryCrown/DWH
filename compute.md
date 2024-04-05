<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Hash searcher</title>
</head>
<body>
    Hash:
    <select id="hash">
        <option value="sha">SHA-512</option>
        <option value="blake">BLAKE2b</option>
        <option value="stree">Streebog</option>
        <option value="sha3">SHA-3</option>
        <option value="fnv0">FNV-0</option>
        <option value="fnv1">FNV-1</option>
        <option value="fnv2">FNV-1a</option>
        <option value="md">MD6</option>
        <option value="jh">JH</option>
        <option value="blake2">BLAKE-512</option>
        <option value="lsh">LSH</option>
        <option value="skein">Skein</option>
        <option value="kec">Keccak3</option>
        <option value="cube">CubeHash</option>
        <option value="whirl0">Whirlpool-0</option>
        <option value="whirl1">Whirlpool-T</option>
        <option value="whirl">Whirlpool</option>
    </select>
    <br>
    <button id="begin" onclick="compute()">Begin!</button>
</body>
</html>
