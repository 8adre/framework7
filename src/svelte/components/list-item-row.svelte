<script>
  import { colorClasses } from '../shared/mixins';
  import { classNames } from '../shared/utils';
  import { restProps } from '../shared/rest-props';

  let className = undefined;
  export { className as class };

  $: classes = classNames(className, 'item-row', colorClasses($$props));
</script>

<div class={classes} {...restProps($$restProps)}>
  <slot />
</div>
