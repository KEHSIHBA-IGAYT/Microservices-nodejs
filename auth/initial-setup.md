npm init -y
npm install typescript ts-node-dev express @types/express
tsc --init

Change the package.json:
"scripts": {
"start": "ts-node-dev src/index.ts"
}

create tsconfig.json:

{
"compilerOptions": {
"target": "es6" /_ Specify ECMAScript target version: 'ES3' (default), 'ES5', 'ES2015', 'ES2016', 'ES2017', 'ES2018', 'ES2019', 'ES2020', or 'ESNEXT'. _/,
"module": "commonjs" /_ Specify module code generation: 'none', 'commonjs', 'amd', 'system', 'umd', 'es2015', 'es2020', or 'ESNext'. _/,
"outDir": "./dist" /_ Redirect output structure to the directory. _/,
"esModuleInterop": true /_ Enables emit interoperability between CommonJS and ES Modules via creation of namespace objects for all imports. Implies 'allowSyntheticDefaultImports'. _/
}
}
